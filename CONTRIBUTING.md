# Contributing

## Who can contribute

- Organizers: see each repo's CODEOWNERS for who reviews it.
- External contributors: please open an issue to discuss before opening a PR.

## Branch model

- `main` is always green. No direct pushes.
- Work in branches named `<type>/<short-slug>`, e.g. `feat/handover-task`, `fix/gripper-tf`, `docs/dataset-format`.
- Open a draft PR early. Mark "Ready for review" when CI is green.

## Pull request process

1. Open a PR against `main`.
2. Where a repo has CI, fix anything red before you request review.
3. Request a review from the relevant CODEOWNERS.
4. Squash-merge. PR title becomes the commit message — see below.

**Heads-up on approvals and merging.** On our public repos, a pull-request approval is **automatically dismissed if you push any new commit after it** (`dismiss_stale_reviews_on_push` is enabled). So get all your commits in _before_ you request review — if you push again after a code owner approves, the approval is voided and you'll need a fresh review before you can merge. The clean sequence: finish your commits → request review → get the code-owner approval → merge without pushing again. (The repo's required status check, where it has one, must be green before merge.)

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
