# Public-Domain Book to EPUB

This project is for bringing old public-domain books from scanned or OCR'd PDF files into clean, modern EPUBs.

The goal is not just conversion. It is editorial cleanup:

- recover readable text from noisy source PDFs
- preserve historical wording where possible
- fix obvious OCR damage and formatting breaks
- restructure content into valid XHTML for EPUB 3
- package the result into a standards-compliant ebook

## What This Repo Does

The workflow in this repo takes a historical source book and moves it through several stages:

1. source PDF intake
2. raw extraction and OCR cleanup
3. chapter-by-chapter XHTML cleanup
4. semantic EPUB structuring
5. final EPUB packaging

In practice, that means turning messy scan output into something that reads like a real ebook instead of a PDF dump.

## Project Layout

- `input/`
  Source materials such as the original PDF. This is treated as generated/archive input and is ignored by git.

- `work/`
  Active working files. This is the one generated-style directory intentionally allowed in version control.

- `work_bk/`
  Backups and raw conversion artifacts. Ignored by git.

- `epub/`
  Assembled EPUB package structure used for building output. Ignored by git.

- `output/`
  Final packaged files such as `.epub`. Ignored by git.

- `real_working_copy/OEBPS/`
  Chapter-by-chapter XHTML cleanup area when doing manual editorial correction.

## Current Focus

This repo is centered on converting older books into:

- valid XHTML
- clean chapter files
- proper footnotes
- improved heading structure
- EPUB 3-compatible packages

## Tooling

The repository includes helper scripts for cleanup and packaging, including:

- `clean_html_to_xhtml.py`
- `build_epub.py`

These support the conversion process, but manual editorial review is still essential. OCR on older books is noisy, and the last mile is usually human cleanup.

## Editorial Principles

- Preserve the original book's wording unless the text is clearly damaged.
- Fix obvious OCR mistakes.
- Remove layout artifacts copied from PDF extraction.
- Keep structure semantic and ebook-friendly.
- Prefer readable, modern EPUBs over facsimile-style exports.

## Output Standard

The intended end state is a modern EPUB 3 book with:

- valid package structure
- semantic XHTML
- working navigation
- readable typography
- cleaned notes and chapter boundaries

## Status

This is an active conversion workspace, not a finished publishing pipeline. Expect a mix of scripts, intermediate files, and manual cleanup targets while books are being processed.
