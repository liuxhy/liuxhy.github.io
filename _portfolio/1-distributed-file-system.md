---
title: "Synchronized Distributed File System"
excerpt: "A gRPC-based distributed file system in C++ with whole-file caching, writer locks, and timestamp-based conflict resolution across concurrent clients."
collection: portfolio
---

A distributed file system that keeps a directory synchronized across multiple clients and a
central server, built in C++ on gRPC.

**Consistency model.** Whole-file caching with single-writer semantics. Clients detect local
changes with CRC32 checksums and resolve conflicts by comparing modification timestamps, so a
stale client never overwrites a newer version on the server.

**Synchronization.** The server holds per-file writer locks and propagates deletions through
async callbacks. Clients watch the local filesystem with `inotify` and hold persistent gRPC
streams open for remote updates, so changes flow in both directions without polling.

**Concurrency.** Mutex-guarded critical sections around the shared file table eliminate race
conditions when several client sessions touch the same path at once.

**Stack:** C++, gRPC, Protocol Buffers, inotify, pthreads

<sub>Built as a graduate coursework project; source is not public under academic integrity policy.
Happy to walk through the design and tradeoffs in conversation.</sub>
