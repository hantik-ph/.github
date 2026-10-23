# Contributing to Hantik

Applies to every repository in the organization unless the repository's own `CONTRIBUTING.md` says otherwise.

## Issues

- **Bug, Feature, Decision.** Pick the form. Blank issues are off.
- One problem per issue. Search first; 👍 an existing one instead of duplicating.
- Title: `<Module>: <one sentence>`. The form sets the `type:` label; add the `area:` label it asks for.
- A **Decision** names one decider. It is not work; it unblocks work.
- An issue is *yours* when you are assigned. Assign yourself before you start.
- Status lives on the **Hantik** project board, not in labels: Backlog → In progress → In review → Done.

## Branches and pull requests

- One issue → one branch `<type>/<issue#>-<slug>` → one pull request.
- Open the PR as a **draft** at the first push, with `Closes #N` in the body. Keep pushing to it; never open a second PR for the same issue.
- Mark it **Ready for review** when done. That runs the full checks and the review.
- PR title is a Conventional Commit; it becomes the squash commit on `main`.
- People merge. Agents and scripts do not.

## Reviews

Every PR gets an automated review and the checks must be green. Changes to authorization, roles, credentials, tenant isolation or the constitution also need a maintainer's approval (see `CODEOWNERS`).

## Security

Never open a public issue for a vulnerability. See [SECURITY.md](SECURITY.md).
