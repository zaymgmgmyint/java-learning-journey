# 10 — Mini Projects

> **Status:** 🔲 Not started
> **Java Version:** Java 21
> **Why it matters:** Theory sticks when you build things. Each mini project is designed to combine multiple modern Java features in a realistic, shareable context.

---

## 🏗️ Project Ideas

| Project | Features Used | Docs | Status |
|---------|--------------|------|--------|
| CLI Task Manager | Records, sealed classes, pattern matching, streams | [task-manager.md](./docs/task-manager.md) | 🔲 |
| Concurrent File Processor | Virtual threads, structured concurrency | [file-processor.md](./docs/file-processor.md) | 🔲 |
| Simple REST Client | HTTP Client, records, Optional, text blocks | [rest-client.md](./docs/rest-client.md) | 🔲 |
| Event Bus | Sealed classes, switch pattern matching, lambdas | [event-bus.md](./docs/event-bus.md) | 🔲 |
| Data Pipeline | Streams, collectors, records, `java.time` | [data-pipeline.md](./docs/data-pipeline.md) | 🔲 |

---

## 🧠 Purpose

These projects are intentionally small (100–300 lines each) — the goal is **demonstrating modern Java idioms in context**, not building full applications. Each one makes good social content because it's focused, readable, and shows clear before/after comparisons with older Java style.

---

## 💡 Tips for Building Each Project

1. Start with the data model using **Records**
2. Define domain types with **Sealed classes**
3. Use **pattern matching** for dispatch logic
4. Process collections with **Streams + Collectors**
5. Handle concurrency (if needed) with **virtual threads**
6. Keep each class under 80 lines — split if needed

---

*[← Back to master index](../README.md)*
