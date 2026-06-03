# ArchSpatialBench Benchmark Design

This document summarizes the public-facing benchmark design. It is intentionally lightweight and does not include private data, model outputs, or copyrighted drawings.

## 1. Goal

ArchSpatialBench evaluates whether multimodal AI models can understand architectural drawings as spatial representations.

The benchmark focuses on a central question:

> Can MLLMs coordinate floor plans, sections, and elevations of a building, or do they rely on language priors and visual templates?

## 2. Why Architectural Drawings

Architectural drawings expose spatial reasoning failures that are not visible in ordinary image benchmarks.

Two properties are central:

1. **Cut-based representation**: plans and sections are cuts through a building, while elevations are projections.
2. **Representational heterogeneity**: real architectural drawings vary in line weight, labels, hatching, scale marks, color, abstraction, and drawing convention.

## 3. Levels

| Level | Focus | Role |
|-------|-------|------|
| L1 | Basic drawing semantics | Perception sanity check |
| L2 | Single-drawing spatial relations | Spatial reasoning baseline |
| L3 | Cross-drawing integration | Main capability target |
| L4 | Geometric precision | Precision ceiling probe |

L3 is the flagship task family because it directly tests architectural drawing coordination across plan, section, and elevation.

## 4. Diagnostic Conditions

| Condition | Meaning |
|-----------|---------|
| V | Visual input + question |
| T | Text-only / question-only blind baseline |
| T+D | Structured textual description + question |
| V+W | Wrong or mismatched image |
| V+R | Rotated image |

These conditions are used to distinguish visual understanding from shortcut behavior.

## 5. Core Data and Wild Data

ArchSpatialBench uses a two-part data strategy:

### Core Data

The redistributable benchmark core. Core Data should contain license-compatible plan / section / elevation matched sets, annotations, questions, and scoring scripts.

Core Data carries the main reproducibility burden.

### Wild Data

The in-the-wild external evaluation split. Wild Data may use published architectural drawings, including ArchDaily-hosted sources, but only under a URL-only policy unless written permission is obtained.

Wild Data should be reported separately from Core Data.

## 6. Release Discipline

- Do not redistribute ArchDaily-hosted images without written permission.
- Do not scrape or bulk-download ArchDaily content without written permission.
- Report Core and Wild results separately.
- Publish annotations, questions, metadata, and evaluation code only when rights allow.
- Include a takedown process for Wild Data metadata / annotations.

## 7. Current Status

The benchmark is under development. The current public repository is a lightweight project page and does not contain benchmark images or private evaluation results.
