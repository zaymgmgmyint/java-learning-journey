# 09 — Java 25 LTS

> **Status:** 🔲 Not started
> **Java Version:** Java 25 (Sep 2025) — LTS
> **Why it matters:** Java 25 is the current LTS and the end goal of this entire learning journey. Everything previewed since Java 21 graduates here. Scoped Values, Stream Gatherers, Flexible Constructors, Module Imports — all stable. Performance is dramatically improved with Compact Object Headers and Generational Shenandoah.

---

## 📚 Topics

| Topic | JEP | Docs | Code | Status |
|-------|-----|------|------|--------|
| Scoped Values (stable) | JEP 506 | [scoped-values-stable.md](./docs/scoped-values-stable.md) | [src/scopedvalues/](./src/) | 🔲 |
| Structured Concurrency (stable) | JEP 505 | [structured-concurrency-stable.md](./docs/structured-concurrency-stable.md) | [src/structured/](./src/) | 🔲 |
| Flexible Constructor Bodies (stable) | JEP 513 | [flexible-constructors-stable.md](./docs/flexible-constructors-stable.md) | [src/constructors/](./src/) | 🔲 |
| Module Import Declarations (stable) | JEP 511 | [module-imports-stable.md](./docs/module-imports-stable.md) | [src/moduleimports/](./src/) | 🔲 |
| Compact Source Files & Instance `main` (stable) | JEP 512 | [compact-source-stable.md](./docs/compact-source-stable.md) | [src/compactsource/](./src/) | 🔲 |
| Primitive Types in Patterns (stable) | JEP 507 | [primitive-patterns-stable.md](./docs/primitive-patterns-stable.md) | [src/primitivepatterns/](./src/) | 🔲 |
| Key Derivation Function API (stable) | JEP 510 | [kdf-api.md](./docs/kdf-api.md) | [src/crypto/](./src/) | 🔲 |
| Compact Object Headers (stable) | JEP 450 | [compact-headers-stable.md](./docs/compact-headers-stable.md) | — | 🔲 |
| Generational Shenandoah GC (stable) | JEP 404 | [shenandoah.md](./docs/shenandoah.md) | — | 🔲 |

---

## 🧠 Module Summary

Java 25 is the **"everything lands" LTS**. After 4 years of incremental previews since Java 21, the type system, concurrency model, and performance story are all complete.

The three features that define modern Java 25 development:

**Scoped Values** replace `ThreadLocal` for virtual-thread-heavy applications — immutable, bounded in scope, and fast. Pair with Structured Concurrency for clean async code without reactive frameworks.

**Compact Source Files & Instance `main`** means Java finally works well as a scripting language — no boilerplate class/public static void main needed for simple programs. Great for tooling and teaching.

**Primitive Types in Patterns** closes the last gap in pattern matching — you can now match on `int`, `long`, etc. directly in switch and instanceof, alongside reference types.

---

## ✨ Java 25 Highlights at a Glance

```java
// Scoped Values — safe, immutable context sharing (replaces ThreadLocal)
static final ScopedValue<String> CURRENT_USER = ScopedValue.newInstance();

ScopedValue.where(CURRENT_USER, "zay").run(() -> {
    processRequest(); // CURRENT_USER.get() → "zay" anywhere in this scope
});

// Flexible Constructor Bodies — run logic before super()
class Circle extends Shape {
    Circle(double radius) {
        if (radius <= 0) throw new IllegalArgumentException("radius must be > 0");
        super(radius * 2); // ← logic before super() now allowed
    }
}

// Primitive Types in Patterns — match int/long/etc. in switch
Object obj = 42;
switch (obj) {
    case Integer i when i > 100 -> System.out.println("large: " + i);
    case Integer i              -> System.out.println("small: " + i);
    case String s               -> System.out.println("text: " + s);
}

// Compact Source File — no class needed for simple programs
void main() {
    System.out.println("Hello from Java 25!");
}

// Module Import — import entire module at once
import module java.base;  // all of java.util, java.io, etc. in one line
```

---

## 🔗 References

- [JEP 506 — Scoped Values](https://openjdk.org/jeps/506)
- [JEP 505 — Structured Concurrency](https://openjdk.org/jeps/505)
- [JEP 507 — Primitive Types in Patterns](https://openjdk.org/jeps/507)
- [JEP 512 — Compact Source Files & Instance Main Methods](https://openjdk.org/jeps/512)
- [JEP 511 — Module Import Declarations](https://openjdk.org/jeps/511)
- [JEP 513 — Flexible Constructor Bodies](https://openjdk.org/jeps/513)
- [JEP 510 — Key Derivation Function API](https://openjdk.org/jeps/510)
- [JDK 25 Release Notes](https://www.oracle.com/java/technologies/javase/25all-relnotes.html)
- [Java 25 LTS and IntelliJ IDEA](https://blog.jetbrains.com/idea/2025/09/java-25-lts-and-intellij-idea/)

---

*[← Back to master index](../README.md)*
