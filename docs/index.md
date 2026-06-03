# ArchSpatialBench

ArchSpatialBench is a benchmark under development for evaluating whether multimodal AI models can reason over architectural drawings.

## What It Tests

The benchmark focuses on spatial reasoning over:

- Floor plans
- Sections
- Elevations
- Cross-view correspondences between plan, section, and elevation

## Why Architecture

Architectural drawings are not ordinary images. Plans and sections are cut-based representations, while elevations are orthographic projections. Reading a building from these views requires reconstructing spatial relationships across heterogeneous drawings.

This makes architecture a strong testbed for distinguishing spatial reasoning from language-prior guessing.

## Data Release Plan

ArchSpatialBench separates data into:

- **Core Data**: redistributable, license-compatible matched drawing sets for the main benchmark.
- **Wild Data**: URL-only in-the-wild evaluation over published architectural drawings. ArchDaily-hosted source images will not be redistributed.

We will not scrape, bulk-download, or redistribute ArchDaily-hosted content without written permission.

## Contact

KAHO LI (李嘉皓)  
PhD Student in Architecture, Tsinghua University  
Email: li-jh22@mails.tsinghua.edu.cn

## Links

- [Benchmark Design](benchmark-design.md)
- [Datasheet Skeleton](project/DATASHEET.md)
- [Data Availability](data.md)
