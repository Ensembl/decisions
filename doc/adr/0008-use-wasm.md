---
tag:Genome Browser
---

# 8. Use Web-Assembly (WASM) for WebGL Wrapper

Date: 2018-08-31

## Status

Accepted

## Consequence of

* [0007-wrap-webgl](0007-wrap-webgl.md)

## Context

ADR-0002 (to wrap WebGL) identified the need for a good place in-browser
for doing data heavy-lifting. Data manipulation in GC-ed environments
tends to suffer easily from jank when there are realtime refresh
constraints. Single-threaded environments (such as the basic model for
in-browser js) are particularly sueecptible.

Browsers offer a number of alternatives to this status quo which take
code out of the event processing loop. These include

* asm.js
* WebWorkers
* Web Assembly

Any of these would have helped. But only the latter offers a
GC-cycle-free environment. Staying inside the JS domain (such as with
web-workers) would also mean needing great care to avoid unnecessary
copies, handle boxing efficiently, GC, etc, due to the JS memory model.

## Decision

Use WASM for efficient data munging.

## Consequences

We need to fine a sane language which can target WASM.
