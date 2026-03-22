# 04 — Java 15–16

> **Status:** 🔲 Not started
> **Java Versions:** Java 15 (Sep 2020), Java 16 (Mar 2021)
> **Why it matters:** Records and sealed classes become production-ready here. This is where modern Java's type system takes shape.

---

## 📚 Topics

| Topic | Version | Docs | Code | Status |
|-------|---------|------|------|--------|
| Records (stable) | Java 16 | [records-stable.md](./docs/records-stable.md) | [src/records/](./src/) | 🔲 |
| Sealed Classes (preview) | Java 15–16 | [sealed-classes.md](./docs/sealed-classes.md) | [src/sealed/](./src/) | 🔲 |
| `instanceof` Pattern Matching (stable) | Java 16 | [instanceof-stable.md](./docs/instanceof-stable.md) | [src/instanceof/](./src/) | 🔲 |
| Text Blocks (stable) | Java 15 | [text-blocks-stable.md](./docs/text-blocks-stable.md) | [src/textblocks/](./src/) | 🔲 |
| Hidden Classes | Java 15 | [hidden-classes.md](./docs/hidden-classes.md) | [src/hidden/](./src/) | 🔲 |

---

## 🧠 Module Summary

Java 15–16 is when previews from 12–14 **graduate to stable**. Records are a game-changer for data carrier classes — replacing verbose POJOs with concise, immutable structures. Sealed classes begin to reshape how you model domain types safely.

Key mindset shift: Java is becoming more expressive and algebraic — think in terms of **data shapes** rather than just objects.

---

## 🔗 References

- [JEP 395 — Records](https://openjdk.org/jeps/395)
- [JEP 397 — Sealed Classes (preview)](https://openjdk.org/jeps/397)
- [JEP 394 — Pattern Matching for `instanceof`](https://openjdk.org/jeps/394)

---

*[← Back to master index](../README.md)*
