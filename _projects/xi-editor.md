---
layout: project
title: Xi-Editor Core
description: A highly performant, modern text editor core written in Rust.
---

**Status:** Active Fork / Core Modernization.
**Language:** Rust (96%), Python (3.4%)
**Original Author:** Raph Levien

---

### About the Project

`xi-editor` is an attempt to build a high-quality text editor using modern software engineering techniques. The original project was officially discontinued by its creator, but we at **Lines of Code** believe its architecture is too good to be abandoned.

We have forked the core and are actively modernizing it to build the backend for our new native frontend, [Lumen](/projects/lumen).

### Our Goals

- **Incredibly high performance:** All editing operations should commit and paint in under 16ms. The editor should never make you wait.
- **Reliability:** Crashing, hanging, or losing work should never happen. The persistent rope data structure ensures safety.
- **Minimalism:** We are stripping away legacy code and updating dependencies to ensure it builds cleanly on recent stable Rust.

### Architecture

The project is split into two distinct parts:

1. **The Core (this repository):** Written in Rust. It holds the file buffers and is responsible for all potentially expensive editing operations.
2. **Frontends:** The Core communicates with frontends via JSON messages. _(Note: We are building our own frontend, Lumen)._

### Getting Started

This repository contains only the editor core, which is not usable on its own. To build the core from the root directory:

```bash
cd rust
cargo build
```

### Why we care

We value transparency and clean architecture. Instead of chasing trends, we focus on writing code that stands the test of time. The `xi-editor` core is a perfect example of this philosophy.
