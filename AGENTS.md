# castastrophe: shared conventions

The defaults for my personal repositories: voice, style, licensing, and the
community health files GitHub inherits from this repo. Individual repos carry their
own `AGENTS.md` for their stack, commands, and testing. This file covers only what
holds across all of them.

For Allons-y Studio work, the equivalent lives in
[allonsy-studio/.github](https://github.com/allonsy-studio/.github/blob/main/AGENTS.md).
The two differ in voice, and that difference is deliberate; see below.

## Voice

These are personal repos, so first person is correct. "I", "me", and "my" belong
here.

This is the one place my conventions and the studio's diverge. Studio copy is
pronoun-free by design, framing everything around what the client gains. That rule
covers client-facing studio material and does not apply here. Don't reconcile the two
by stripping the pronouns out of a personal README.

Otherwise: plain, direct, and specific. No hedging, no filler, no jargon where a
plain word does the job.

## Style guide

Chicago Manual of Style, with these exceptions.

| Element             | Use                             | Not                               |
| ------------------- | ------------------------------- | --------------------------------- |
| Section titles      | "About me"                      | "About Me", "ABOUT ME"            |
| Hyphenated compound | "Front-end"                     | "Front-End"                       |
| Conjunction         | "systems & design"              | "systems and design"              |
| Numbers             | "12+ years"                     | "twelve-plus years"               |
| Months              | "November"                      | "Nov"                             |
| Dates               | "2027 January 15", "2027-01-15" | "January 15, 2027", "01-15-2027"  |
| Date ranges         | "2014 January–2021 July"        | "January 2014 - July 2021"        |
| Dashes              | "scannable: nothing buried"     | "scannable — nothing buried"      |

Dates are year-first in both forms. Ranges take an en dash (–), not a hyphen. The
Oxford comma stays. Prefer `:` over em dashes, in prose, commit bodies, and PR
descriptions alike.

## Licensing

Pick by the project's scope & impact:

- **MPL-2.0**: open-source, small, low-impact, or non-monetizable projects.
- **Apache-2.0**: high-impact or monetizable projects.

Under a `## License` heading in the README, use the matching text:

> [MPL-2.0](LICENSE): use freely, modify as needed; changes to MPL-licensed files
> should be shared back under the same license.

> [Apache-2.0](LICENSE): use freely, modify as needed; includes an express patent
> grant from contributors. Retain the license & attribution notices when
> redistributing.

## Commits and pull requests

Conventional Commits, and [CONTRIBUTING.md](CONTRIBUTING.md) has the full flow: branch
naming, commit types, and PR guidelines.

Commit and PR bodies are either notes for my future self or summaries for collaborators or open source users. Keep any reasoning that won't be obvious in 6+ months; drop the rest.

- PR descriptions: 1 to 3 sentences of prose by default, ~100 words at most. Lead with a
  verb; never open with "This PR".
- Commit bodies: 1 to 2 sentences, or none for a small change.
- Leave out environment or sandbox notes, after-merge process, file lists the diff already
  shows, speculation about causes, side findings (open an issue instead), unfilled
  template comments, and an empty `Closes #`.
- Test plan: one line on what was actually checked.
- Review replies: one sentence plus the commit SHA.
- No headers beyond the template's, no bold-label bullets, no em dashes.

Never add AI attribution to a commit or a PR: no `Co-Authored-By` trailer, no
"Generated with …" footer, no session URLs. This holds in every repo, without
exception.

## What GitHub inherits from here

Any of my repositories that lacks its own copy falls back to the files in this repo:
[CODE_OF_CONDUCT.md](CODE_OF_CONDUCT.md), [CONTRIBUTING.md](CONTRIBUTING.md),
[SECURITY.md](SECURITY.md), [SUPPORT.md](SUPPORT.md),
[PULL_REQUEST_TEMPLATE.md](PULL_REQUEST_TEMPLATE.md), the
[issue templates](ISSUE_TEMPLATE/), and `FUNDING.yml`. A repo that needs something
different overrides it locally rather than editing these.
