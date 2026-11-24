---
aliases:
  - L6
tags:
  - networking/osi
  - networking/layer6
creation_date: 2026-11-06
source: scrib2
up: "[[OSI]]"
---

# Presentation layer (L6)

Receives data from the [[Application layer]] (words, numbers, human-readable stuff) and converts it into a form machines can process, basically **binary**.

**Jobs:**
- **Translation**: character encodings, data formats
- **Compression**
- **Encoding**
- **Encryption**: SSL/TLS
- **Abstraction**: apps don't care how data is represented on the wire

Next layer down: [[Session layer]] · up to [[OSI]]
