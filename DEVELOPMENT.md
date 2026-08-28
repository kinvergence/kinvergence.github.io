# Development

Working notes for `index.html`. Read this before changing copy.

The *scope* decisions and their reasoning live in
[kinvergence-core `ROADMAP.md` § 3a](https://github.com/kinvergence/kinvergence-core/blob/main/ROADMAP.md).
This file carries what is repo-local: how to work on the page, what must not be reintroduced, and
which facts have been checked against sources.

---

## Why the site is this small

Deliberately, and the reasoning is the framework's own. Adoption is a *basin* problem: a family
cannot be handed the framework, so a comprehensive website is a document handoff — precisely what
the model predicts will not work. A big-bang framework site was scoped, argued against, and
**rejected on 2026-08-25**.

Every element is judged by one test: **does this make somebody's first meeting more likely to
actually happen?** If not, cut it.

The page also has to survive its own advice. Getting Started tells an adopting family to skip the
name, the logo, and the website. The site says so about itself, in section 2. Do not add anything
that makes that paragraph a lie.

## Who it is for

**The audience is a family, not a person.** Every sentence's subject is *a family*; the reader is
never assigned the role of entrepreneur. This is what lets the same page work for a peer, for a
parent thinking about their children, and for a visitor who arrived from something other than a
personal conversation.

The likely first visitor is someone a member spoke to in person. Assume warm arrival. There is no
SEO play and no funnel.

## Hard copy constraints

Violating any of these is a defect, not a style preference.

| Rule | Source |
|---|---|
| **No mathematics, no notation.** The model is linked, never imported | `docs/kinvergence.md`, hard constraint |
| **No "Kin-" vocabulary.** No KinShip, no Kinnections. Heartbeat and Demo Day keep their ordinary names | Declined 2026-08-06; `docs/glossary.md` § Words we don't use |
| **No "methodology", "program", "system", "membership", "curriculum"** — each implies something the framework is not | `docs/glossary.md` |
| **No emoji.** Not as decoration, not as icons | `docs/brand/visual-identity.md` correction banner |
| **No cumulative counts** — no "285+ meetings", no "5.5 years". They go stale and the figures in circulation did not survive checking. Use dated events and "almost every week since \<date\>" | See § Checked facts |
| **No singular "they"** for one person. Rewrite the sentence | Ed's standing convention |
| **US spelling** | — |
| **Nothing in the footer may imply an open license or a settled owner** | `docs/adoption/instances.md` § A note on the framework's own status |

## Do not reintroduce

The structural skeleton came from `scherer-frailey-ventures.github.io/family-ventures-framework-2.html`.
Its *content* is wrong in ways that are easy to carry back in by accident:

- **A "Core Values" section asserting universal values.** This contradicts the framework's own claim
  that values are what each *instance* names for itself. The single worst thing to restore.
- **Four "pillars"** that are not the framework's practices — the list includes shared tooling,
  which is on Getting Started's skip-list *on purpose*.
- **Emoji as decorative icons.**
- **FVF-era branding** and `[Qualifier] Family Ventures`.
- **Its teal/green palette** — a third, separately-arrived-at scheme with no authority.
- **The draft banner.** Dropped deliberately: the page is meant to be sent to someone.

## Checked facts

Verified against SFV's own archives. The reconstruction, with an evidence grade on every row, is
[SFV's timeline](https://github.com/scherer-frailey-ventures/commons/blob/main/docs/sfv-timeline.md)
and its
[methodology companion](https://github.com/scherer-frailey-ventures/commons/blob/main/docs/sfv-timeline-methodology.md).

| Claim | Status |
|---|---|
| Founded **2020-09-11** | Verified |
| **~20 informal months** before anything repeated | Verified. 26 messages in the whole of 2021 — but this means *no artifact obligation*, **not** that nothing happened. Never write "nothing happened" |
| Agenda + standing weekly slot proposed **2022-05-23** | Verified |
| Name "Heartbeat" first used **2022-06-06** | Verified |
| Demo Day proposed 2022-06-27 for 2022-08-01; **first actually held 2022-08-08** (postponed, illness) | Corrected 2026-08-26. The page says only "Aug 2022" and describes the *proposal* as being for the first of August — both still accurate. Do not add a day-level date |
| Discord adopted **2022-08-09**, the day after the first Demo Day | Corrected 2026-08-26 (earlier stated as eight days). The page carries no number here — keep it that way |
| "Almost every week since" | Verified 2026-08-26 from the Discord archive: 163 of 212 weeks, six short gaps of ≤3 weeks in four years |
| "Weekly rhythm since 2022", *not* 2021 or "six years" | The 2021 claim was wrong and published; it is corrected at source |

**If a new claim needs a number, check it against the timeline first, and prefer a dated event.**

## Decisions in force

Settled with Ed on 2026-08-25. Reopen deliberately, not by drift.

| Element | Decision |
|---|---|
| **Audience** | A family, not a named reader |
| **Hero** | Lead with the twenty-month false start, not with duration |
| **Ask** | Give permission to leave first, then ask for correction rather than agreement |
| **Ask destination** | **No link.** The reader is asked to go back to the member who sent them. The Discord server is invitation-only by design, so linking it publicly would contradict `docs/reference/discord-server.md` |
| **Honest limits** | Split — the load-bearing one inside the ask as its justification, the rest immediately below under their own heading. Never collapsed, never greyed, never framed as a disclaimer |
| **Section order** | SFV's story leads. It is the only real evidence |
| **Depth** | Only the Heartbeat gets a "try this" treatment. Demo Day, stewardship and the charter get a sentence and a link |

### Swap-ready hero alternates

Both were approved in the same pass and can be dropped in directly:

- *"One family has met almost every week for four years — after taking nearly two years to find a shape that stuck."*
- *"The agreement came in 2020. The rhythm took another two years."*

## Brand

**Provisional.** Palette and marks are taken from
[`docs/brand/assets/`](https://github.com/kinvergence/kinvergence-core/tree/main/docs/brand/assets)
— the only palette the shipped assets actually embody:

| Role | Hex |
|---|---|
| Attractor / accent | `#FFD166` |
| Structural | `#3D5A80` |
| Ink | `#2B2B33` |
| Paths (mark only) | `#E63946` `#2EC4B6` `#6A4C93` `#3D5A80` |

The full brand pass — candidate marks against the model's Part IV filters, reconciling the three
competing palettes, extending the diagnostic visual language — is **postponed, not cancelled**
(`ROADMAP.md` § 3c). Do not start it here.

## Verification checklist

Before calling any change done:

- [ ] Renders correctly at **375px, 768px and 1440px**
- [ ] Mobile nav toggle opens, closes on link click, and `aria-expanded` tracks state
- [ ] `prefers-reduced-motion` honored — animation and smooth scroll both disabled
- [ ] No external network requests. No fonts, no analytics, no CDNs
- [ ] Headings in order, skip link works, focus rings visible, AA contrast
- [ ] All four section anchors reachable from the nav
- [ ] Copy re-checked against **Hard copy constraints** and **Checked facts** above

## Deploying

GitHub Pages serves `main` at the repo root. Pushing publishes.

**For `kinvergence.org`:** add a `CNAME` file containing the bare domain and point DNS at GitHub
Pages. The site is built so that this is the *only* change required — every internal link is a
fragment or relative, and no absolute `github.io` URL appears anywhere.

## Open questions

- **Should the site name members?** It currently does not — "one member", "somebody". Naming Julia
  and Derek where they are quoted would add real credibility and costs some privacy. Not yet decided.
- **Does the ask get an address?** Currently no link at all, which is defensible on its own. A
  `kinvergence.org` mailbox would be a one-line change.
- **Should it be indexable?** Currently yes. There is no SEO play, but no reason to hide it either.
- **Feedback from Ed and Julia is pending** as of 2026-08-27 and has not been applied.

## History

- **2026-08-25** — Built. Single page, four sections, verified at three widths. Nothing about the
  page's factual claims has needed changing since, including through the 2026-08-26 timeline
  corrections — a consequence of the no-cumulative-counts rule rather than luck.
