# Datasheet for ArchSpatialBench

Status: public skeleton. Full datasheet will be completed before a formal benchmark release.

## 1. Motivation

ArchSpatialBench was created to evaluate whether multimodal large language models genuinely understand architectural drawings or rely on language-prior shortcuts.

The benchmark targets floor plans, sections, and elevations, with special emphasis on cross-drawing spatial coordination.

## 2. Creator

Created by KAHO LI (李嘉皓), PhD student in Architecture at Tsinghua University, as part of PhD research.

Advisor / lab details: TBD.

## 3. Composition

The intended benchmark contains two splits:

- **Core Data**: redistributable plan / section / elevation matched sets with images, annotations, questions, and scoring code.
- **Wild Data**: URL-only published architectural drawings for in-the-wild evaluation. Source images are not redistributed.

## 4. Data Access and Distribution

Core Data will be distributed directly once licensing and release scope are finalized.

Wild Data will not include source image files. Public materials may include:

- Source URLs
- Project metadata
- Checksums
- Project annotations created by the benchmark team
- Benchmark questions
- Evaluation scripts

ArchDaily-hosted source images will not be redistributed without written permission.

## 5. Ethical and Copyright Notes

The project will not scrape, bulk-download, or redistribute ArchDaily-hosted content without written permission.

If Wild Data entries are included, a takedown process will be documented.

## 6. License

TBD. Code, Core Data, and Wild Data metadata may use different licenses depending on rights and release constraints.
