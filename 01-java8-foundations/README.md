# 01 — Java 8 Foundations

> **Status:** 🔲 Not started
> **Java Version:** Java 8 (March 2014)
> **Why it matters:** Java 8 was the biggest shift in the language's history — it introduced functional programming concepts and remains the baseline for most enterprise codebases today.

---

## 📚 Topics

| Topic | Docs | Code | Status |
|-------|------|------|--------|
| Lambda Expressions | [lambdas.md](./docs/lambdas.md) | [src/lambdas/](./src/) | 🔲 |
| Functional Interfaces | [functional-interfaces.md](./docs/functional-interfaces.md) | [src/functional/](./src/) | 🔲 |
| Stream API | [streams.md](./docs/streams.md) | [src/streams/](./src/) | 🔲 |
| Optional | [optional.md](./docs/optional.md) | [src/optional/](./src/) | 🔲 |
| Method References | [method-references.md](./docs/method-references.md) | [src/methodrefs/](./src/) | 🔲 |
| Default & Static Interface Methods | [interface-methods.md](./docs/interface-methods.md) | [src/interfaces/](./src/) | 🔲 |
| `java.time` API | [datetime.md](./docs/datetime.md) | [src/datetime/](./src/) | 🔲 |
| Collectors | [collectors.md](./docs/collectors.md) | [src/collectors/](./src/) | 🔲 |

---

## 🧠 Module Summary

Java 8 moved Java from an imperative-only language to one that supports **functional-style programming**. The core idea: pass behavior (functions) as data, and process collections declaratively via pipelines.

Key shift in mindset:
- **Before:** `for` loops everywhere, anonymous inner classes for callbacks
- **After:** lambdas, method references, stream pipelines

---

## 🔗 References

- [JEP 126 — Lambda Expressions](https://openjdk.org/jeps/126)
- [Java 8 Release Notes](https://www.oracle.com/java/technologies/javase/8-relnotes.html)

---

*[← Back to master index](../README.md)*
