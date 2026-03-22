# 07 — Java 21 LTS

> **Status:** 🔲 Not started
> **Java Version:** Java 21 (Sep 2023) — LTS
> **Why it matters:** Java 21 is the current gold standard. Virtual threads are stable, pattern matching is complete, and the language feels genuinely modern. This is where you want to be.

---

## 📚 Topics

| Topic | Docs | Code | Status |
|-------|------|------|--------|
| Virtual Threads (stable) | [virtual-threads-stable.md](./docs/virtual-threads-stable.md) | [src/virtualthreads/](./src/) | 🔲 |
| Structured Concurrency (preview) | [structured-concurrency.md](./docs/structured-concurrency.md) | [src/structured/](./src/) | 🔲 |
| Pattern Matching for `switch` (stable) | [switch-patterns-stable.md](./docs/switch-patterns-stable.md) | [src/switchpatterns/](./src/) | 🔲 |
| Record Patterns (stable) | [record-patterns-stable.md](./docs/record-patterns-stable.md) | [src/recordpatterns/](./src/) | 🔲 |
| `SequencedCollection` (stable) | [sequenced-stable.md](./docs/sequenced-stable.md) | [src/sequenced/](./src/) | 🔲 |
| Unnamed Classes & Instance `main` (preview) | [unnamed-classes.md](./docs/unnamed-classes.md) | [src/unnamed/](./src/) | 🔲 |
| String Templates (preview) | [string-templates.md](./docs/string-templates.md) | [src/stringtemplates/](./src/) | 🔲 |

---

## 🧠 Module Summary

Java 21 is the **"everything is ready" LTS**. Virtual threads alone are worth upgrading for — they make Java competitive with Go and Node.js for I/O-bound workloads without changing your programming model. Pattern matching for switch allows expressive, exhaustive type-safe dispatch that rivals Kotlin and Scala.

If you're targeting one version for modern Java content — **this is it**.

---

## ✨ Java 21 Highlights at a Glance

```java
// Virtual threads — simple to use
try (var executor = Executors.newVirtualThreadPerTaskExecutor()) {
    executor.submit(() -> handleRequest(req));
}

// Pattern matching for switch
String result = switch (shape) {
    case Circle c    -> "Circle with radius " + c.radius();
    case Rectangle r -> "Rectangle " + r.width() + "x" + r.height();
    default          -> "Unknown shape";
};

// Record patterns
if (obj instanceof Point(int x, int y)) {
    System.out.println("Point at " + x + ", " + y);
}
```

---

## 🔗 References

- [JEP 444 — Virtual Threads](https://openjdk.org/jeps/444)
- [JEP 441 — Pattern Matching for `switch`](https://openjdk.org/jeps/441)
- [JEP 440 — Record Patterns](https://openjdk.org/jeps/440)
- [JEP 431 — `SequencedCollection`](https://openjdk.org/jeps/431)
- [Java 21 Release Notes](https://www.oracle.com/java/technologies/javase/21-relnote-issues.html)

---

*[← Back to master index](../README.md)*
