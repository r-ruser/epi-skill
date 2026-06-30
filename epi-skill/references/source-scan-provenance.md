# Source Scan Provenance

This skill was distilled from local full-page scans of the user's supplied PDFs on 2026-06-30.
The scan artifacts are stored at:

`C:\Users\cbl02\Desktop\ai_skills_hub\epi_skill_full_scan`

Each source has a folder containing `pages.jsonl`, `method_hits.jsonl`, and `summary.json`.
The scan records page number, text length, SHA-1 hash of extracted page text, keyword counts,
section candidates, and short previews. The skill itself does not copy textbook chapters or long
source passages.

## Full-Page Scan Summary

| Source | Pages | Text pages | Low-text pages | Method-hit pages | Engine |
|---|---:|---:|---:|---:|---|
| 13578524_高级医学统计学=Advancedmedicalstatistics.pdf | 521 | 0 | 521 | 0 | pdfminer; OCR probe available |
| 34、生物信息学 8年制第2版_李霞，雷健波主编2015.pdf | 526 | 0 | 526 | 0 | pdfminer; OCR probe available |
| Biostatistics Epidemiology UWorld notes | 23 | 18 | 5 | 14 | pdfminer |
| Fundamentals of Biostatistics, Rosner | 891 | 890 | 1 | 648 | pdfminer |
| Medical Statistics at a Glance, 4e | 211 | 204 | 7 | 175 | pdfminer |
| Modern Epidemiology, 4th | 2324 | 2317 | 7 | 2127 | pdfminer |
| The New Statistics with R | 277 | 265 | 12 | 164 | pdfminer |
| Understanding Advanced Statistical Methods | 572 | 557 | 15 | 383 | pdfminer |
| 数学手册(原书第10版) | 1577 | 1573 | 4 | 208 | pypdfium2 fallback |
| 现代流行病学 第3版 | 974 | 0 | 974 | 0 | pypdfium2; OCR probe available |

## OCR Status

Three Chinese scanned PDFs have no extractable text layer. A RapidOCR probe was installed and
validated at render scale 1.0. Probe output is stored at:

`C:\Users\cbl02\Desktop\ai_skills_hub\epi_skill_full_scan\ocr`

The OCR script is:

`C:\Users\cbl02\Desktop\ai_skills_hub\tools\ocr_low_text_pages.py`

Run without `--max-pages-per-pdf` for full OCR continuation when needed. The skill content is based
on the completed full-page text-layer scan, OCR quality probes for scanned PDFs, and methodologic
distillation rather than verbatim source transfer.

## Main Method Signals

- Modern Epidemiology 4th: dense coverage of design, bias, confounding, measurement, causal inference, prediction/diagnosis, regression, and effect measures.
- Rosner Fundamentals: dense coverage of regression, prediction/diagnosis, measurement, survival, effect measures, study design, confounding, and bias.
- Medical Statistics at a Glance: compact coverage of study design, measurement, bias, regression, survival, reporting, and effect measures.
- The New Statistics with R: useful for regression, interaction, estimation-oriented thinking, and biological examples.
- Understanding Advanced Statistical Methods: useful for probabilistic thinking, Bayesian/resampling topics, regression, measurement, and advanced interpretation.
- Chinese scanned sources were fully page-enumerated and have OCR-ready artifacts, but their text layer is absent.
