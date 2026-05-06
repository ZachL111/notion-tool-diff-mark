# notion-tool-diff-mark

`notion-tool-diff-mark` is a Python project in cli tools. Its focus is to package a Python local lab for diff analysis with framed sample traffic, bounds and ordering tests, and documented operating limits.

## Project Rationale

The project exists to keep a narrow engineering decision visible and testable. For this repo, that decision is how file span and argument risk should influence a review result.

## Notion Tool Diff Mark Review Notes

The first comparison I would make is `file span` against `argument risk` because it shows where the rule is most opinionated.

## Feature Set

- `fixtures/domain_review.csv` adds cases for file span and terminal width.
- `metadata/domain-review.json` records the same cases in structured form.
- `config/review-profile.json` captures the read order and the two review questions.
- `examples/notion-tool-diff-walkthrough.md` walks through the case spread.
- The Python code includes a review path for `file span` and `argument risk`.
- `docs/field-notes.md` explains the strongest and weakest cases.

## Architecture

The core code exposes a scoring path and the added review layer uses `signal`, `slack`, `drag`, and `confidence`. The domain terms are `file span`, `terminal width`, `argument risk`, and `report density`.

The added Python path is deliberately direct, with fixtures doing most of the explaining.

## Usage

```powershell
powershell -NoProfile -ExecutionPolicy Bypass -File scripts/verify.ps1
```

## Test Command

That command is also the regression path. It verifies the domain cases and catches mismatches between the CSV, metadata, and code.

## Next Improvements

The repository is intentionally scoped to local checks. I would expand it by adding adversarial fixtures before adding features.
