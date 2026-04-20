---
name: survey-dataset-evolution
description: Use when the user wants an academic survey, literature review, or benchmark analysis about evaluation dataset generation and evolution, especially evaluation dataset evolution success rate, temporal longitudinal evolution, dynamic dataset updates, adaptive evolution, multimodal temporal benchmarks, source reliability, and compute-cost reporting. This skill is specialized for producing or updating Chinese Markdown survey documents in the Survey_results workspace with authoritative citations and consistent terminology.
---

# Survey Dataset Evolution

Use this skill when the task is to build, extend, or polish a survey on benchmark dataset generation and evolution, especially around `评测数据集演化成功率`.

## Default output target

- First look for `Survey_results/survey.md` and `Survey_results/总结.md`.
- Treat those two files as the primary integrated outputs unless the user explicitly asks for separate files.
- If split files already exist under `Survey_results/`, reuse them instead of recreating structure.

## Scope this skill is optimized for

- Temporal longitudinal evolution of benchmarks
- Time-sliced / streaming benchmark construction
- Dynamic dataset updates and live benchmarks
- Adaptive / drift-triggered evolution
- Evolution success-rate definitions, proxies, and metrics
- Multimodal temporal benchmarks
- Training cost and GPU-hour reporting with reliability checks

## Workflow

1. Read the current `Survey_results` documents before editing.
2. Preserve the established terminology and section structure unless the user asks for a rewrite.
3. When discussing methods, organize around categories rather than paper-by-paper narration.
4. When discussing metrics, separate:
   - model performance
   - benchmark evolution success
5. When discussing costs, separate:
   - training cost
   - benchmark update cost
   - human / API / maintenance cost
6. If the user asks about multimodal work, use the distinction in `references/context.md` between:
   - process-type temporal longitudinality
   - semantic-type temporal longitudinality
7. If the user asks for GPU-hours or compute cost, apply the reliability rubric in `references/context.md` and do not invent exact card-hours.

## Source policy

- Prefer official proceedings and official archival pages:
  - ACL Anthology
  - PMLR
  - NeurIPS proceedings / NeurIPS Datasets and Benchmarks
  - OpenReview pages for officially accepted papers
  - TACL / TMLR official pages
- Distinguish source tiers in prose when useful:
  - flagship conference / journal
  - Findings / Datasets and Benchmarks track
  - accepted OpenReview page
- If a number is coarse, say so explicitly.

## Writing policy

- Default to Chinese Markdown.
- Keep claims conservative and source-grounded.
- When a unified definition does not exist in the literature, say it is a synthesized framework or inferred abstraction.
- Favor tables for:
  - method taxonomy
  - representative papers
  - cost comparisons
  - multimodal benchmark comparisons
- Favor short concluding paragraphs over long bullet dumps.

## Existing project conventions

- The canonical integrated survey lives in `Survey_results/survey.md`.
- The compressed final summary lives in `Survey_results/总结.md`.
- Topic files under `Survey_results/` are supporting artifacts, not replacements.
- The survey already uses a stable success-rate framing based on `Q/F/C/G/R/L/E`.
- The survey already contains a multimodal section and a GPU-hour special investigation; extend those instead of duplicating them.

## Read when needed

- For project-specific terminology, file map, multimodal benchmark set, and GPU-hour reliability rules, read [references/context.md](references/context.md).
