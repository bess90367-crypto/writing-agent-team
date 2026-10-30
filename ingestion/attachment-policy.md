# Attachment Ingestion Policy

## Goal

When the user provides a PDF, image, or spreadsheet for a task, inspect its contents in a suitable readable or structured form before drafting and distilling reusable knowledge.

## PDF workflow

1. Prefer the PDF's embedded text layer when available.
2. Inspect page layout visually when tables, forms, stamps, annotations, or scan quality could affect meaning.
3. For image-only/scanned pages, use visual reading/transcription; use OCR only when necessary.
4. Preserve page boundaries or headings when they matter.
5. Normalize obvious extraction artifacts without silently changing substantive wording.

## Image workflow

1. Read the image visually.
2. Transcribe relevant text into structured Markdown.
3. Preserve visible hierarchy: title, labels, table rows, dates, annotations.
4. Mark uncertain text rather than guessing.

## Spreadsheet workflow

When a user asks for a message based on a workbook or a supplied example/template:
1. Inspect the actual workbook and the relevant example before describing what is wrong or asking for a correction.
2. Check headings, rows, formulas/totals, and whether the requested change is **individual breakdown → aggregate total** or the reverse; do not infer direction from a brief description alone.
3. Separate what the file shows from what the user says the receiving office requires. If the file cannot be inspected, do not claim to have verified its contents.

## Learning workflow

After reading or extraction:
1. identify factual content needed for the current task;
2. identify durable writing/administrative rules;
3. separate one-off facts from reusable knowledge;
4. store reusable learning in the appropriate `knowledge/` file;
5. add a regression case if the source reveals a recurring failure mode.

## Public repository handling

The repository is public by user choice. Prefer committing distilled/redacted learning rather than unnecessary raw personal correspondence. If the raw extracted text itself is important as a reusable source, store it under `knowledge/sources/` with enough context to understand what it teaches.
