# Contributing

## Who can contribute

- Organizers: see each repo's CODEOWNERS for who reviews it.
- External contributors: please open an issue to discuss before opening a PR.

## Branch model

- `main` is always green. No direct pushes to repos with a branch ruleset; the rest are maintained by direct commit under the maintainers' review convention.
- Work in branches named `<type>/<short-slug>`, e.g. `feat/handover-task`, `fix/gripper-tf`, `docs/dataset-format`.
- Open a draft PR early. Mark "Ready for review" when any required checks are green (some repos have none).

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

## Repository-specific guidance

Setup, tooling (linting, formatting, tests), and the details a bug report needs differ per repository, so this guide stays repo-agnostic. For anything repo-specific, see the README in the repository you're contributing to, and use that repository's issue templates, where provided, to report bugs.
