# Contributing

## Who can contribute

- Organizers: see OWNERSHIP.md for repo stewards.
- External contributors: please open an issue to discuss before opening a PR.

## Branch model

- `main` is always green. No direct pushes.
- Work in branches named `<type>/<short-slug>`, e.g. `feat/handover-task`, `fix/gripper-tf`, `docs/dataset-format`.
- Open a draft PR early. Mark "Ready for review" when CI is green.

## Pull request process

1. Open a PR against `main`.
2. CI runs lint + tests. Fix anything red.
3. Request a review from the relevant CODEOWNERS.
4. Squash-merge. PR title becomes the commit message — see below.

## Commit / PR title format

`<type>: <imperative summary>`, e.g. `feat: add pick-and-place baseline`.

Allowed types: `feat`, `fix`, `docs`, `test`, `refactor`, `chore`, `perf`.

This is the only convention we enforce.

## Local setup

```bash
pip install -e ".[dev]"
pre-commit install
pre-commit run --all-files
pytest
```

## Code style

Run `pre-commit run --all-files` before pushing. CI will fail otherwise.

## Reporting bugs

Use the issue templates. Include OS, Python version, sim version, and a minimal reproducer.
