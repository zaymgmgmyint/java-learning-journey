# 08 — Java 22–24

> **Status:** 🔲 Not started
> **Java Versions:** Java 22 (Mar 2024), Java 23 (Sep 2024), Java 24 (Mar 2025)
> **Why it matters:** This era bridges Java 21 LTS to Java 25 LTS. Stream Gatherers, Foreign Function & Memory API, unnamed variables, and structured concurrency all stabilize or preview here. Performance gets a major boost in Java 24.

---

## 📚 Topics

| Topic | Version | Docs | Code | Status |
|-------|---------|------|------|--------|
| Stream Gatherers | Java 22 (preview) → 24 (stable) | [stream-gatherers.md](./docs/stream-gatherers.md) | [src/streamgatherers/](./src/) | 🔲 |
| Foreign Function & Memory API (stable) | Java 22 | [ffm-api.md](./docs/ffm-api.md) | [src/ffm/](./src/) | 🔲 |
| Unnamed Variables & Patterns (stable) | Java 22 | [unnamed-variables.md](./docs/unnamed-variables.md) | [src/unnamed/](./src/) | 🔲 |
| Statements Before `super()` | Java 22 (preview) → 25 (stable) | [flexible-constructors.md](./docs/flexible-constructors.md) | [src/constructors/](./src/) | 🔲 |
| Structured Concurrency (preview rounds) | Java 22–23 | [structured-concurrency.md](./docs/structured-concurrency.md) | [src/structured/](./src/) | 🔲 |
| Scoped Values (preview rounds) | Java 22–23 | [scoped-values.md](./docs/scoped-values.md) | [src/scopedvalues/](./src/) | 🔲 |
| Primitive Types in Patterns | Java 23 (preview) | [primitive-patterns.md](./docs/primitive-patterns.md) | [src/primitivepatterns/](./src/) | 🔲 |
| Module Import Declarations | Java 23 (preview) | [module-imports.md](./docs/module-imports.md) | [src/moduleimports/](./src/) | 🔲 |
| Compact Source Files & Instance `main` | Java 23 (preview) | [compact-source.md](./docs/compact-source.md) | [src/compactsource/](./src/) | 🔲 |
| Quantum-Resistant Cryptography (KEM/KDF) | Java 24 | [crypto.md](./docs/crypto.md) | [src/crypto/](./src/) | 🔲 |
| Compact Object Headers | Java 24 (experimental) | [compact-headers.md](./docs/compact-headers.md) | — | 🔲 |
| G1 Region Pinning | Java 22 | [g1-pinning.md](./docs/g1-pinning.md) | — | 🔲 |

---

## 🧠 Module Summary

Java 22–24 is a **busy bridge era** — lots of features cycling through preview rounds on their way to Java 25 LTS. Two standouts:

**Stream Gatherers** (stable in Java 24) let you write your own intermediate stream operations — think custom windowing, grouping, or de-duplication directly in a pipeline. This fills the one gap Streams had since Java 8.

**Foreign Function & Memory API** (stable in Java 22) lets Java call native code and manage off-heap memory safely — replaces the fragile `sun.misc.Unsafe` and JNI patterns.

Java 24 also focuses heavily on **performance**: compact object headers reduce object memory footprint, G1 improvements reduce GC pauses, and virtual thread pinning issues are resolved.

---

## ✨ Highlights at a Glance

```java
// Stream Gatherers — custom intermediate operation (Java 24)
List<List<Integer>> windows = Stream.of(1, 2, 3, 4, 5)
    .gather(Gatherers.windowFixed(2))
    .toList();
// → [[1, 2], [3, 4], [5]]

// Unnamed variables — ignore what you don't need (Java 22)
try {
    int result = Integer.parseInt(input);
} catch (NumberFormatException _) {   // ← _ means "don't care"
    System.out.println("Invalid input");
}

// Scoped Values — safe alternative to ThreadLocal (Java 23 preview)
ScopedValue<String> USER = ScopedValue.newInstance();
ScopedValue.where(USER, "zay").run(() -> {
    System.out.println(USER.get()); // → "zay"
});
```

---

## 🔗 References

- [JEP 461 — Stream Gatherers (preview)](https://openjdk.org/jeps/461)
- [JEP 485 — Stream Gatherers (stable, Java 24)](https://openjdk.org/jeps/485)
- [JEP 454 — Foreign Function & Memory API](https://openjdk.org/jeps/454)
- [JEP 456 — Unnamed Variables & Patterns](https://openjdk.org/jeps/456)
- [JEP 480 — Structured Concurrency (Java 23 preview)](https://openjdk.org/jeps/480)
- [JEP 487 — Scoped Values (Java 23 preview)](https://openjdk.org/jeps/487)

---

*[← Back to master index](../README.md)*
