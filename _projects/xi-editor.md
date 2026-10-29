---
layout: default
title: Xi-Editor Core
description: A highly performant, modern text editor core written in Rust.
---

<div class="container project-content">
  <h1>Xi-Editor Core</h1>
  <p><strong>Status:</strong> Active Fork / Core Modernization.</p>
  <p><strong>Language:</strong> Rust (96%), Python (3.4%)</p>
  <p><strong>Original Author:</strong> Raph Levien</p>

  <hr>

  <h3>About the Project</h3>
  <p><code>xi-editor</code> is an attempt to build a high-quality text editor using modern software engineering techniques. The original project was officially discontinued by its creator, but we at <strong>Lines of Code</strong> believe its architecture is too good to be abandoned.</p>
  <p>We have forked the core and are actively modernizing it to build the backend for our new native frontend, <a href="/projects/lumen">Lumen</a>.</p>

  <h3>Our Goals</h3>
  <ul>
    <li><strong>Incredibly high performance:</strong> All editing operations should commit and paint in under 16ms. The editor should never make you wait.</li>
    <li><strong>Reliability:</strong> Crashing, hanging, or losing work should never happen. The persistent rope data structure ensures safety.</li>
    <li><strong>Minimalism:</strong> We are stripping away legacy code and updating dependencies to ensure it builds cleanly on recent stable Rust.</li>
  </ul>

  <h3>Architecture</h3>
  <p>The project is split into two distinct parts:</p>
  <ol>
    <li><strong>The Core (this repository):</strong> Written in Rust. It holds the file buffers and is responsible for all potentially expensive editing operations.</li>
    <li><strong>Frontends:</strong> The Core communicates with frontends via JSON messages. <em>(Note: We are building our own frontend, Lumen).</em></li>
  </ol>

  <h3>Getting Started</h3>
  <p>This repository contains only the editor core, which is not usable on its own. To build the core from the root directory:</p>

```bash
cd rust
cargo build
```

  <h3>Why we care</h3>
  <p>We value transparency and clean architecture. Instead of chasing trends, we focus on writing code that stands the test of time. The <code>xi-editor</code> core is a perfect example of this philosophy.</p>
</div>
