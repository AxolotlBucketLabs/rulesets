# AxolotlBucketLabs Rulesets

This repository stores the versioned GitHub ruleset configuration used by AxolotlBucketLabs repositories.

## Main baseline

The `main-baseline` directory contains one importable JSON export for each repository that uses the `main-baseline` ruleset. The files preserve repository-specific required status checks while keeping the review, branch, and bypass policy consistent.

The ruleset requires one approval, requires the latest push to be approved by another person, dismisses stale approvals, requires resolved review conversations, blocks branch deletion and force pushes, and targets the `main` branch. The `NhanAZ` user is the only configured bypass actor so the organization owner can push directly when necessary.

Status check names belong to the repository that produced them. If a workflow is renamed, its corresponding JSON export must be updated before the ruleset is imported again.

## Layout

- `main-baseline/` contains the current ruleset exports.
- `.github/workflows/validate.yml` validates every JSON export on pushes and pull requests.
- `LICENSE` contains the MIT license for the original repository documentation and configuration.

These files describe GitHub repository settings. They do not apply themselves to repositories. Changes must be reviewed, imported, and verified against the live GitHub ruleset separately.
