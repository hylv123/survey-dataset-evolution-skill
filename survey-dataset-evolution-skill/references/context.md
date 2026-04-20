# Project Context

This reference captures the durable context from the current survey project so future work can continue with the same assumptions and terminology.

## Canonical files

- `Survey_results/survey.md`: primary integrated survey
- `Survey_results/总结.md`: compressed final summary
- `Survey_results/04_多模态专题.md`: multimodal-focused supporting document
- `Survey_results/14_张卡时专项调研.md`: detailed GPU-hour investigation
- `Survey_results/15_张卡时专项调研总结.md`: compressed GPU-hour summary
- `Survey_results/06_严格多模态_时间纵向benchmark论文.md`: strict multimodal + temporal-longitudinal benchmark list

## Core research topic

Primary topic:

- benchmark dataset generation and evolution

Primary subtopic:

- evaluation dataset evolution success rate

Priority angles:

- temporal longitudinal evolution
- time-series / temporal evolution
- dynamic dataset updates
- adaptive dataset evolution
- multimodal temporal benchmarks

## Established method taxonomy

The project has already converged on these major categories:

1. adversarial human-in-the-loop iterative evolution
2. time-sliced / streaming evolution
3. self-updating benchmark construction
4. live benchmark / contamination-limited benchmark
5. drift-aware and adaptive evolution
6. multimodal temporal and dynamic extensions

## Success-rate framework

Use the existing seven-dimension framing unless the user asks to replace it:

- `Q`: data quality
- `F`: freshness
- `C`: challenge
- `G`: longitudinal generalization
- `R`: evaluation reliability
- `L`: contamination control
- `E`: cost efficiency

Important distinction:

- model performance answers whether the model is good
- evolution success answers whether the benchmark update was good

## Multimodal conventions

The project distinguishes two kinds of temporal longitudinality:

- `process-type temporal longitudinality`
  - the sample itself unfolds along real time
  - representative examples:
    - `Terra`
    - `TUMTraf VideoQA`
    - `DanmakuTPPBench`
    - `MTBBench`
    - `MC-BEC`
    - `Time-IMM`

- `semantic-type temporal longitudinality`
  - the temporal axis is primarily historical, cultural, or semantic
  - representative example:
    - `Hanfu-Bench`

When the user asks about dynamic updates or evolution success rate, prioritize process-type benchmarks.

## Current authoritative multimodal paper set

These papers have already been accepted into the survey as reliable multimodal references:

- `VisIT-Bench`
- `Terra`
- `TUMTraf VideoQA`
- `DanmakuTPPBench`
- `Hanfu-Bench`
- `MTBBench`
- `MC-BEC`
- `Time-IMM`

Preferred source types for those papers:

- NeurIPS proceedings / NeurIPS Datasets and Benchmarks
- ICML / PMLR
- EMNLP / ACL Anthology
- OpenReview official accepted pages

## GPU-hour investigation conventions

The project already established that GPU-hour data are sparse in this literature.

Always distinguish:

- benchmark update cost
- baseline model training cost
- full project compute cost
- human / API / maintenance cost

Use this reliability rubric:

- `A`: explicit GPU type + count + time, directly citable
- `B`: mostly explicit, but scope must be qualified
- `C`: coarse quantity only, such as "hundreds of GPU hours"
- `D`: hardware info only, relative steps only, or local timing only

Known strong examples:

- `DynaQuest`
  - `12 H100 GPU-hours`
  - `8 H100 GPU-hours`
  - `0.67 H100 GPU-hours` for a filtering step
  - treat training cost and benchmark update cost separately
- `LAMM`
  - `24 A100 GPU hours`
  - baseline model training cost, not a long-term benchmark update cost

Known weak or coarse examples:

- `OrQA`: only "hundreds of GPU hours on four A100"
- `StreamingQA`: relative step reduction, not standardized GPU-hours
- `Time-IMM`: module-level timing, not full card-hours
- `OSAMD/OACA`: hardware environment only

## Writing constraints already adopted in the project

- Chinese Markdown output
- clear sectioning suitable for proposal or midterm report reuse
- conservative wording for claims
- explicit source reliability language when needed
- avoid overstating "strictly satisfies" unless the boundary has been discussed

## Maintenance rule

If you extend this survey:

- update `survey.md` first
- then sync the key conclusion into `总结.md`
- only create new topic files when the user explicitly asks for a separate artifact
