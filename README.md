# ArchSpatialBench

**Can multimodal AI models understand architectural drawings?**

ArchSpatialBench is a research benchmark under development for evaluating spatial reasoning over architectural drawings, including floor plans, sections, and elevations.

The benchmark asks whether multimodal large language models (MLLMs) can establish spatial correspondences across architectural projections, or whether they rely on language priors and visual templates.

## Research Question

When a multimodal model sees architectural drawings, does it actually reason over spatial structure, or does it guess from linguistic and visual priors?

The central capability of interest is architectural "drawing coordination": mapping between plan, section, and elevation views of the same building.

## Benchmark Structure

ArchSpatialBench is organized around four levels:

| Level | Focus | Example capability |
|-------|-------|--------------------|
| L1 | Basic semantics | Identify rooms, floors, building type |
| L2 | Single-drawing spatial reasoning | Relative position, adjacency, orientation |
| L3 | Cross-drawing integration | Match plan, section, and elevation information |
| L4 | Geometric precision | Coordinates, proportions, simplified geometry matching |

It also uses controlled experimental conditions:

| Condition | Input | Purpose |
|-----------|-------|---------|
| V | Drawing + question | Standard visual QA |
| T | Question only | Blind language-prior baseline |
| T+D | Structured textual description + question | Text reasoning vs visual interpretation |
| V+W | Wrong / mismatched drawing + question | Wrong-image resistance |
| V+R | Rotated drawing + question | Rotation consistency |

## Data Strategy

The project separates the benchmark into two data splits:

### Core Data

The redistributable benchmark core. It will use self-authored, synthetic, license-friendly, or open 3D / BIM-derived plan-section-elevation matched sets. Core Data is intended to support reproducible benchmarking, long-term hosting, and leaderboard-style evaluation.

### Wild Data

An in-the-wild evaluation split based on publicly published architectural drawings, including ArchDaily-hosted projects. Wild Data is URL-only: source images are not redistributed. Only source URLs, metadata, checksums, project annotations, benchmark questions, and evaluation code may be released.

We will not scrape, bulk-download, or redistribute ArchDaily-hosted content without written permission.

## Current Status

This repository is a lightweight public project page. The full benchmark, data, and evaluation code are still under development.

Current priorities:

- Build a redistributable Core Data split.
- Clarify permission and release policy for ArchDaily-based Wild Data.
- Expand L3 cross-drawing tasks and human ceiling evaluation.
- Prepare a dataset datasheet and benchmark protocol for a future academic submission.

## Contact

KAHO LI (李嘉皓)  
PhD Student in Architecture  
Tsinghua University  
Email: li-jh22@mails.tsinghua.edu.cn

## License

License is pending. The benchmark will distinguish between code, redistributable Core Data, and URL-only Wild Data.
