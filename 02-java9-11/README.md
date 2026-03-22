# 02 — Java 9–11

> **Status:** 🔲 Not started
> **Java Versions:** Java 9 (Sep 2017), Java 10 (Mar 2018), Java 11 LTS (Sep 2018)
> **Why it matters:** Java 11 is still heavily used in production. This era introduced the module system, `var`, and a proper HTTP client.

---

## 📚 Topics

| Topic | Version | Docs | Code | Status |
|-------|---------|------|------|--------|
| Module System (JPMS) | Java 9 | [modules.md](./docs/modules.md) | [src/modules/](./src/) | 🔲 |
| `var` — Local Variable Type Inference | Java 10 | [var.md](./docs/var.md) | [src/var/](./src/) | 🔲 |
| New HTTP Client API | Java 11 | [http-client.md](./docs/http-client.md) | [src/httpclient/](./src/) | 🔲 |
| String API Additions | Java 11 | [string-api.md](./docs/string-api.md) | [src/stringapi/](./src/) | 🔲 |
| `List.of` / `Map.of` / `Set.of` | Java 9 | [immutable-collections.md](./docs/immutable-collections.md) | [src/collections/](./src/) | 🔲 |
| `Optional` Improvements | Java 9–11 | [optional-updates.md](./docs/optional-updates.md) | [src/optional/](./src/) | 🔲 |
| `Stream` Improvements | Java 9–11 | [stream-updates.md](./docs/stream-updates.md) | [src/streams/](./src/) | 🔲 |

---

## 🧠 Module Summary

This era is defined by **modularity and convenience**. Java 9's JPMS was controversial but solved real dependency hell problems. Java 10's `var` reduced boilerplate without sacrificing type safety. Java 11 (LTS) cleaned up the API and is still a supported baseline in many organizations.

---

## 🔗 References

- [JEP 261 — Module System](https://openjdk.org/jeps/261)
- [JEP 286 — `var` Local Variable Type Inference](https://openjdk.org/jeps/286)
- [JEP 321 — HTTP Client](https://openjdk.org/jeps/321)

---

*[← Back to master index](../README.md)*
