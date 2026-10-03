---
name: Proje notu sıkılaştırma (Dashboard)
description: 02-projeler içindeki notunu tek dosyada yüksek yoğunluklu bir kontrol paneline dönüştürür
placement: append
order: 13
---
Refactor and compress the referenced project note in-place into a high-density, single-file project dashboard:

1. Structural Invariants:
   - Preserve the exact YAML frontmatter and primary heading taxonomy.
   - Do not split the document into external files or introduce non-existent wiki-links. Maintain single-file integrity.

2. Executive Metric Table:
   - Place a compact Markdown table directly below the summary blockquote capturing: Current Version (with commit hash), Tech Stack, Embedded/Vendored Dependencies, Layout/Architecture (e.g., Pitchfork), Test Suite & Sanitizer Coverage, Key Optimizations, Process/Security Isolation, and Remote Repo.

3. Task & Log Consolidation:
   - Purge micro-level task checkboxes, verbose commit-by-commit prose, terminal dumps, and inline code blocks.
   - Collapse completed tasks into concise SemVer milestone items (e.g., `- [x] v1.0.0 — <summary>`).
   - Keep the Log section strictly limited to major version release dates and essential commit hashes.

4. Engineering Core & Metric Preservation:
   - Condense architectural decisions (ADRs) and root-cause fixes into dense, single-bullet takeaways (e.g., memory safety/UAF fixes, POSIX shell-free execution, batching optimizations, async event handling).
   - Retain all concrete metrics (e.g., test counts, percentage call reductions, latency limits, complexity bounds).
