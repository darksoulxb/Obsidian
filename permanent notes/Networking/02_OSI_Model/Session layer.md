---
aliases:
  - session layer
  - L5
tags:
  - networking/osi
  - networking/layer5
creation_date: 2026-11-06
source: scrib2
up: "[[OSI]]"
---

# Session layer (L5)

Establishes, manages, synchronizes, and terminates connections ("sessions") between two communicating applications.

1. **Session establishment**
2. **Session maintenance**: checkpoints to recover from errors without restarting everything
3. **Session termination**

> [!warning] Correction
> Scrib put "divided into small chunks known as segments" and "sequence numbers coordinate segments" here. That's **segmentation**, which belongs to the [[Transport layer]] ([[TCP]]).

Next layer down: [[Transport layer]]
