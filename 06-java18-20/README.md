# 06 — Java 18–20

> **Status:** 🔲 Not started
> **Java Versions:** Java 18 (Mar 2022), Java 19 (Sep 2022), Java 20 (Mar 2023)
> **Why it matters:** Project Loom (virtual threads) starts previewing here — one of the biggest concurrency improvements in Java's history. Structured concurrency introduces a safer mental model for async code.

---

## 📚 Topics

| Topic | Version | Docs | Code | Status |
|-------|---------|------|------|--------|
| Virtual Threads (preview) | Java 19 | [virtual-threads.md](./docs/virtual-threads.md) | [src/virtualthreads/](./src/) | 🔲 |
| Structured Concurrency (preview) | Java 19–20 | [structured-concurrency.md](./docs/structured-concurrency.md) | [src/structured/](./src/) | 🔲 |
| Pattern Matching for `switch` (preview) | Java 18–20 | [switch-patterns.md](./docs/switch-patterns.md) | [src/switchpatterns/](./src/) | 🔲 |
| Record Patterns (preview) | Java 19–20 | [record-patterns.md](./docs/record-patterns.md) | [src/recordpatterns/](./src/) | 🔲 |
| UTF-8 by Default | Java 18 | [utf8.md](./docs/utf8.md) | — | 🔲 |
| Simple Web Server | Java 18 | [simple-webserver.md](./docs/simple-webserver.md) | [src/webserver/](./src/) | 🔲 |
| `SequencedCollection` (preview path) | Java 20 | [sequenced.md](./docs/sequenced.md) | [src/sequenced/](./src/) | 🔲 |

---

## 🧠 Module Summary

This era is dominated by **Project Loom** — virtual threads are lightweight threads managed by the JVM rather than the OS. The implication: you can spawn millions of threads without the overhead that made thread-per-request architectures impractical.

Key mindset shift: concurrency in Java is about to get much simpler. Forget reactive programming for I/O-bound work — virtual threads make blocking code scale.

---

## 🔗 References

- [JEP 425 — Virtual Threads (preview)](https://openjdk.org/jeps/425)
- [JEP 428 — Structured Concurrency (incubator)](https://openjdk.org/jeps/428)
- [JEP 427 — Pattern Matching for `switch` (preview)](https://openjdk.org/jeps/427)

---

*[← Back to master index](../README.md)*
