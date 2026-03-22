# 05 — Java 17 LTS

> **Status:** 🔲 Not started
> **Java Version:** Java 17 (Sep 2021) — LTS
> **Why it matters:** Java 17 is the most widely targeted LTS after Java 11. Sealed classes finalize here, and the JVM gets stronger encapsulation. Many teams are migrating to or targeting this version right now.

---

## 📚 Topics

| Topic | Docs | Code | Status |
|-------|------|------|--------|
| Sealed Classes (stable) | [sealed-stable.md](./docs/sealed-stable.md) | [src/sealed/](./src/) | 🔲 |
| Pattern Matching Progress | [pattern-matching.md](./docs/pattern-matching.md) | [src/patterns/](./src/) | 🔲 |
| Strong Encapsulation of JDK Internals | [encapsulation.md](./docs/encapsulation.md) | [src/encapsulation/](./src/) | 🔲 |
| Deprecations & Removals | [deprecations.md](./docs/deprecations.md) | — | 🔲 |
| `RandomGenerator` API | [random.md](./docs/random.md) | [src/random/](./src/) | 🔲 |
| Context-Specific Deserialization Filters | [serialization.md](./docs/serialization.md) | [src/serial/](./src/) | 🔲 |

---

## 🧠 Module Summary

Java 17 is the **"settle in" LTS** — everything previewed in 12–16 is now stable and safe to use in production. The JVM also tightens security by fully removing access to internal APIs.

If your team is still on Java 11, **Java 17 is your next upgrade target** and understanding what changed is essential.

---

## 🔗 References

- [JEP 409 — Sealed Classes](https://openjdk.org/jeps/409)
- [JEP 403 — Strongly Encapsulate JDK Internals](https://openjdk.org/jeps/403)
- [Java 17 Release Notes](https://www.oracle.com/java/technologies/javase/17-relnote-issues.html)

---

*[← Back to master index](../README.md)*
