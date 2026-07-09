# AGENTS.md

## Cursor Cloud specific instructions

### What this repository is
This is a **data / content repository**, not a software project. There is no
application, service, build system, package manifest, test suite, or lint config.
Do not look for `package.json`, `Dockerfile`, a dev server, ports, etc. — none
exist. "Running the application" is not applicable; the deliverables are documents
and data.

Contents:
- `main` branch: a single Excel workbook,
  `20260114 Data AI 2025 December - Consolidated.xlsx` — a multi-sheet research
  dataset (sheets include `Projects`, `ProjectsFR`, `Data`, `consultative tables`,
  `TranslationScreens`, `Land Register`, `E-filing`, `E-Auction`,
  `Private providers`, `Case law database`, `Sources`). This is the core artifact.
- Feature branches (`cursor/tygodniowy-przegl-d-ai-*`): Polish-language Markdown
  "Tygodniowy przegląd AI" (Weekly AI Review) reports.
- `hyperlink-audit-report` branch: a PDF auditing hyperlinks used in the reports.

### Working with the content
- The Excel workbook can be read/validated with Python + `openpyxl` (installed by
  the startup update script). Quick sanity check from the repo root:

  ```python
  import openpyxl
  wb = openpyxl.load_workbook(
      "20260114 Data AI 2025 December - Consolidated.xlsx",
      read_only=True, data_only=True)
  print(wb.sheetnames)
  ```

- Markdown reports are plain text; no tooling required to edit them.
- There is nothing to lint, test, or build. If asked to "run tests" or "build",
  clarify that this repo has none.

### Gotchas
- The Excel filename contains spaces — always quote it in shell commands.
- Branches diverge significantly (the Markdown reports do not live on `main`);
  check out the relevant branch before editing a specific report.
