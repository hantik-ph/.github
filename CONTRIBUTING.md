# Contributing to Hantik

This guide lives in the organization's `.github` repository and applies to every
`hantik-ph` repository that has no `CONTRIBUTING.md` of its own.

## How work flows

1. **Features start from an issue.** A feature or a behaviour change is filed
   first through one of the forms: Bug, Feature or change, or Question, so the
   design is agreed before the code. A fix, chore or docs change may go
   straight to a pull request. Blank issues are off. A Question
   is a decision, not work: when it is decided, the answer goes in a comment,
   the issue is closed, and the work is filed as a Bug or a Feature.
2. **Take it before you start it.** Assign yourself. An unassigned issue is a
   promise that nobody is on it.
3. **A pull request is one logical change.** A feature or behaviour change
   starts from an issue; a fix, chore or docs change needs none. Open a draft
   pull request whose body lists `Closes #<n>` for each issue it finishes and
   `Refs #<n>` for each it only advances, and answers every bold heading of the org
   `PULL_REQUEST_TEMPLATE.md`. Keep pushing to that PR; a large issue lands as
   a series of small PRs, each one step; one change is never split by file
   or area into several PRs. Branch names are plain
   (`fix/rent-roll-refund`); GitHub keeps the link to the issue, not the name.
4. **A person marks it ready, and a person merges.** Marking ready runs the
   full gate and the review. Agents and scripts never merge, never mark a PR
   ready, and never push to `main`.
5. **The gate.** Where the repository has `./scripts/verify.sh`, it must pass
   on the exact commit before every push (`quick` on a draft, `gate` to merge).
   Where it does not, the repository's CI is the gate. A red check is not
   argued with; it is fixed. `--no-verify` is not an option.

## Commit messages

- Subject in [Conventional Commits](https://www.conventionalcommits.org/) form:
  `type(scope): what changes`, where `type` is `feat`, `fix`, `chore`, `docs`,
  `ci`, `spec` or `test`. The PR title uses the same form; it becomes the
  squash commit on `main`.
- The body says **why**: what was wrong, what changed, and what was
  deliberately not done. The diff already says what. If a check was added, say
  how it was proved to fail before it passed.
- Trailers go last, after a blank line (`Assisted-by`, `Co-Authored-By`,
  `Closes` belongs in the PR body, not the commit).

## AI-assisted contributions

AI tools are welcome here, under the same terms the
[Fedora AI-Assisted Contributions Policy](https://docs.fedoraproject.org/en-US/council/policy/ai-contribution-policy/)
and the
[OpenSSL AI Code and Documentation Contribution Policy](https://openssl-library.org/policies/general/ai-policy/)
(June 2026) set out.

- **You are the author.** The human who opens the pull request is accountable
  for every line in it, however it was produced. You have read it, you
  understand it, and you have run it. "The model wrote that" is not a defence
  in review, and a PR you cannot explain is not ready.
- **Disclose by trailer.** When a non-trivial part of a change was produced by
  an AI tool, say so with a commit trailer naming the tool and the model:

  ```
  Assisted-by: Claude Code claude-fable-5-1
  ```

  This is the Fedora and kernel convention; OpenSSL writes the same trailer as
  `Assisted-by: {agent}:{model}`, and either spelling is accepted. The
  `Co-Authored-By: Claude ...` trailer that Claude Code writes on its own
  commits counts as this disclosure; you do not need to add a second line.
  Autocomplete of a line, reformatting and spell-checking need no trailer.
  If in doubt, disclose.
- **AI is never the only reviewer.** An automated review is advice. It does not
  substitute for a passing gate, and it is never the final judge of whether a
  change merges. A person reads the diff and a person approves.
- **No orphan PRs.** A pull request opened by an agent with no human owner who
  answers for it is closed without review. Reopen it under your own name when
  you have read and tested it.
- **No secrets, no client data.** A tool that pastes either into a diff is
  your responsibility. Finding one means stop and report, not quietly delete.

## Security

Never open a public issue for a vulnerability. See [SECURITY.md](SECURITY.md).
