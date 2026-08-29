# Development

Working notes for the site. Read this before changing copy.

The *scope* decisions and their reasoning live in
[kinvergence-core `ROADMAP.md` § 3a](https://github.com/kinvergence/kinvergence-core/blob/main/ROADMAP.md).
This file carries what is repo-local: how to work on the pages, what must not be reintroduced, and
which facts have been checked against sources.

## Structure

Four pages, no build step. Shared styles in `assets/site.css`, the nav toggle in `assets/site.js`.
Nav markup, footer, and the inlined marks are duplicated per page deliberately — **change them in
all four or they drift.**

| Page | Job | Words |
|---|---|---:|
| `index.html` | The invitation. Nothing here that is not needed to make a first meeting more likely | ~1,240 |
| `story.html` | How the practice actually formed, with dates, quotations, and the corrections | ~1,600 |
| `heartbeat.html` | How to run one, the three failure modes, what to skip, what comes after | ~990 |
| `honesty.html` | Untested claims, falsifiers, our own errors, and the ownership question | ~875 |

**The home page is the constrained one.** It was 1,996 words on 2026-08-25 and is now ~1,240. Two
rounds of sentence-level trimming got it only to 1,710; the rest came from moving whole blocks onto
the three pages above. If it grows again, move material out — do not trim. That has been tried
twice and does not work.

Each home-page section ends in an `.onward` link. **That pattern is load-bearing:** a short section
that visibly opens onto more reads deliberate, and a short section that simply stops reads thin.

### The cadence diagram

`index.html` § 3 carries the site's only non-text element: three rows over a twelve-column grid —
twelve weekly beats, three monthly markers aligned to beats 4, 8 and 12, and one unbroken band.
Pure CSS grid, no image, no SVG beyond the marks already inlined.

**It is an argument, not decoration, and the third row is the argument.** The continuous practice
has no occasion, which is exactly why it leaves no record and why an adopting family loses it
without noticing — the framework's own open claim, rendered. The monthly markers align with weekly
beats deliberately: Demo Day takes the same slot and stands in for that week's call rather than
adding to it, which is a real finding from the archive.

The tracks are `aria-hidden`; the `figcaption` states the pattern in words. **Do not add rows, do
not animate it, and do not reuse it on the interior pages** — there is no templating layer, so a
second copy would drift.

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
| **First person, always.** The site is written *by* the family it describes. Never "they", "one member", "somebody" for SFV. Third-person narration forces circumlocutions and reads as evasive | Adopted 2026-08-27; see § History |
| **Members are named.** Ed, Julia, Derek, Jason, Helen. First names only | Decided 2026-08-27 |
| **No mathematics, no notation.** The model is linked, never imported | `docs/kinvergence.md`, hard constraint |
| **No "Kin-" vocabulary.** No KinShip, no Kinnections. Heartbeat and Demo Day keep their ordinary names | Declined 2026-08-06; `docs/glossary.md` § Words we don't use |
| **No "methodology", "program", "system", "membership", "curriculum"** — each implies something the framework is not | `docs/glossary.md` |
| **No emoji.** Not as decoration, not as icons | `docs/brand/visual-identity.md` correction banner |
| **No cumulative counts** — no "285+ meetings", no "5.5 years". They go stale and the figures in circulation did not survive checking. Use dated events and "almost every week since \<date\>" | See § Checked facts |
| **No links into `kinvergence-core`.** It is private and stays private — see § The repository is not the publication | Decided 2026-08-27 |
| **No singular "they"** for one person. Rewrite the sentence | Ed's standing convention |
| **US spelling.** No contractions in the site's own voice — "do not", not "don't". Quotations are exempt and are reproduced verbatim | — |
| **Nothing in the footer may imply an open license or a settled owner** | `docs/adoption/instances.md` § A note on the framework's own status |

## The repository is not the publication

**Decided 2026-08-27.** `kinvergence-core` is **private and stays private.** It is the working
corpus — rough, provenance-stamped, unratified, and largely unreviewed. This site is the
publication. Material is *promoted* here as curated pages after review; it is never linked to in
place.

Three reasons, in ascending force:

1. **Audience.** The target reader is a non-technical person a member spoke to. Dropping that
   person into a GitHub repo is a bad handoff regardless of content quality.
2. **It is the rejected plan through a side door.** A big-bang framework site was rejected on
   2026-08-25 because it would freeze MVP-grade, unreviewed synthesis as public canon. Linking the
   repo is the same content exposure with none of the editing.
3. **The framework's own model.** Adoption is a *basin* problem; a repo link is the maximal
   document handoff. And with ownership and license unsettled until 2026-09-07, publishing the whole
   corpus is precisely what `ROADMAP.md` calls gating.

Seven dead GitHub links were removed on 2026-08-27 as a result. Section 3 now ends with a promise
(*"We are writing all of that up properly. It will be here."*) rather than a link. **That promise is
a commitment — do not leave it unredeemed, and do not redeem it with a link back into the corpus.**

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
| **Audience** | A family, not a named reader. *(The reader is a family; the narrator is us. These are separate decisions — do not collapse them.)* |
| **Voice** | First person, members named. Adopted 2026-08-27 |
| **Hero** | Lead with the twenty-month false start, not with duration |
| **Ask** | Give permission to leave first, then ask for correction rather than agreement |
| **Ask destination** | **No link.** The reader is asked to go back to the member who sent them. The Discord server is invitation-only by design, so linking it publicly would contradict `docs/reference/discord-server.md` |
| **Honest limits** | The load-bearing one (*we cannot tell from the inside*) stays inside the ask on `index.html` at full weight. The rest live on `honesty.html`. **This reopened the 2026-08-25 "never collapsed, never moved" decision** — see § The limits, and why they moved |
| **Section order** | SFV's story leads. It is the only real evidence |
| **Depth** | Only the Heartbeat gets a "try this" treatment on the home page. Everything else is a curated page on this site |
| **Ask section color** | Deep navy (`--slate-deep`), not near-black. Footer follows in `--navy-deep`. Changed 2026-08-27 on Julia's reaction |

### The limits, and why they moved

On 2026-08-25 it was decided that the honest limits must be *"never collapsed, never greyed, never
framed as a disclaimer."* On 2026-08-27 four of the five moved to `honesty.html` anyway, to get the
home page short enough to actually be read. Ed's call, made explicitly rather than by drift: the
more recent concern overrides the earlier one.

**The guard, which is the whole basis for allowing it:**

- The load-bearing limit stays on the home page, inside the ask, at full weight, as the ask's own
  justification. It is not a caveat there and must not become one.
- The link to `honesty.html` is a prominent `.onward` line and **must never become a footnote**.
- `honesty.html` leads with the n=1 problem in a callout, states what would prove the framework
  wrong, and carries the unsettled ownership question. **Do not soften any of it to make the site
  more appealing.** If that page ever gets quieter, vaguer, or harder to reach, the 08-25 decision
  was right and this one was a mistake.

### Swap-ready hero alternates

Both were approved in the same pass and can be dropped in directly (restated in first person
2026-08-27):

- *"We have met almost every week for four years — after taking nearly two years to find a shape that stuck."*
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

Before calling any change done — **on every page you touched**:

- [ ] Renders correctly at **375px, 768px and 1440px**
- [ ] Mobile nav toggle opens, closes on link click, and `aria-expanded` tracks state
- [ ] `prefers-reduced-motion` honored — animation and smooth scroll both disabled
- [ ] No external network requests. No fonts, no analytics, no CDNs. `assets/` is same-origin and fine
- [ ] Headings in order, skip link works, focus rings visible, AA contrast
- [ ] Every internal link resolves to a file that exists, and no link points into `kinvergence-core`
- [ ] Nav and footer identical across all four pages, with `aria-current="page"` on the right item
- [ ] Copy re-checked against **Hard copy constraints** and **Checked facts** above

## Deploying

GitHub Pages serves `main` at the repo root. Pushing publishes.

**`kinvergence.org` is live** as of 2026-08-27, along with `www.kinvergence.org`. The `CNAME` file
in the repo root holds the bare domain and is committed. **Do not delete or rewrite it**, and pull
before committing if the custom domain was reconfigured through the GitHub Pages UI — GitHub commits
`CNAME` on its own side, and clobbering it takes the domain down. Every internal link is a fragment
or relative; no absolute `github.io` URL appears anywhere.

## Open questions

- **Does the ask get an address?** Currently no link at all, which is defensible on its own. A
  `kinvergence.org` mailbox would be a one-line change.
- **Should it be indexable?** Currently yes. There is no SEO play, but no reason to hide it either.
- **Contractions.** The site's own voice uses full forms throughout ("do not", "cannot"), which
  contributes to the formality Julia flagged as "AI slop." Changing it is a whole-page voice
  decision, deliberately deferred to her concision pass rather than made unilaterally.
- **More visual language?** The cadence diagram is the first non-text element and is currently the
  only one. Anything further — rendering alignment, drift, or cadence health as checkable states —
  is the model's Part IV diagnostic language and belongs to the deferred brand pass, not here.

### Settled

- **Should the site name members?** **Yes** — decided 2026-08-27. Ed, Julia, Derek, Jason, Helen,
  first names only. Both the credibility gain and the anti-"AI slop" effect were larger than
  expected; the privacy cost is small, since all four are already public on the SFV site.

## Feedback awaiting action

**Julia, via the SFV Telegram group, night of 2026-08-27 — her first read of the Pass 2 four-page
site.** Recorded as evidence, not yet applied — Ed's attention moved to `advance-sfv-2.md` the next
day. Apply before Julia's reunion (09-18) and before treating Pass 2 as done.

| She said | Reading / action |
|---|---|
| Liked the four-page split; "Skip to the practice" vs. "Start from the beginning" — "like a quick start option when you buy a new tool" | Validates the Pass 2 structural bet. No action |
| Timeline "so, so cool"; found it interesting/inspiring despite having lived it; "leaving no trace... so important" | `story.html`'s no-trace argument (open claim 2) lands even for a member who was there. No action |
| "What we got wrong" is "illuminating... people will like seeing that, haha" | `honesty.html`'s errors section works as intended. No action |
| "This does *not* read like AI slop at all" | Direct reversal of her Pass 1 reaction. The first-person, named-members voice fix worked. No action |
| Confused by "Carried in the open…" under "What we do not know" — asked whether it means the limits are freely exposed for others to observe or modify | **Actionable.** Ambiguous even to a sympathetic reader on a second pass. Needs a clearer rephrase on `honesty.html` |
| "The one that matters most: YES. This sums up the purpose of the site succinctly and clearly" | The load-bearing limit (kept at full weight per § The limits, and why they moved) is landing as intended. No action |
| Liked the list of things never tested | No action |
| Loved *"Nobody has ever asked a family outside ours whether they want any of this... you are among the first to be asked"* — "I'd highlight it in some way" | **Actionable.** Consider a visual callout/pull-quote treatment on `honesty.html` |
| "Who holds this" — "interesting... will do so [think about it] when the time is right" | Ownership question landing as intended; she's holding it for the 09-07 Demo Day conversation, not asking for a site change |
| The "Put it on the calendar" ask at the bottom "did not jump out... in fact, I nearly missed it. Perhaps it was the blue color" | **Actionable, and the most important item here** — the ask is the whole point of the site and is under-visible. See tension note below |
| "Cut to the chase" (short) path "worked just fine... ample information without being overwhelming" | Validates the "Skip to the practice" quick-start path |
| Expects first-time visitors to go back and forth between long and short, "like thumbing through the chapters of a book" | Validates the dual-path navigation model |

Sign-off: *"Well done, Little Brother. I like this direction."*

**Tension with an existing decision.** The ask section's color was changed to deep navy specifically
on 2026-08-27 because of an earlier Julia reaction against near-black. This new reaction — the same
section barely noticed, "perhaps... the blue color" — could mean that fix undershot, or that
visibility here is a weight/size/whitespace problem rather than a hue problem. Needs a fresh look at
the section as a whole, not just another color swap.

## History

- **2026-08-27 — Pass 2: three curated pages, and the home page finally gets short.** Split into
  four pages with shared `assets/site.css` and `assets/site.js`. The home page went 1,710 → ~1,170
  words, **41% below the 2026-08-25 original**, which is what Pass 1's editing could not achieve on
  its own.

  **The structural point:** Ed's *"there should be deeper content"* and Julia's *"way too wordy"*
  looked like opposite instructions and were the same one — *move depth off the front page*. Nothing
  was deleted; the front page got shorter and the site got deeper in the same operation.

  `story.html` and `honesty.html` also carry material the site has never shown a reader before: the
  corrections we have made to our own published history, and an explicit statement of what would
  falsify the framework. Both are stronger arguments than anything that was cut.

  Also: the honest-limits decision was deliberately reopened — see § The limits, and why they moved.

  **The cadence diagram** was added in the same pass — see § The cadence diagram. It is the site's
  first non-text element and it answers Ed's request to show *a little structure* without importing
  any of the model's notation.

- **2026-08-27 — Pass 1: voice, concision, correctness.** Ed's and Julia's feedback applied. The
  whole page moved into first person with members named.

  **On length, the honest number: body copy fell from 1,996 words to 1,710 — 14%, not the third
  that was aimed for.** Two rounds of cutting were run and the second produced diminishing returns.
  The reason is worth recording, because it will recur: **what is left is not padding, it is
  structure.** Per section — story 526, practice 442, the ask 337, hopes 297, hero 108. Nothing
  above is filler; three of those blocks are page-worth content sitting on a front page. Shaving
  further degrades the writing without meaningfully shortening the read. **The remaining reduction
  has to come from moving content onto separate pages, not from editing sentences** — which is what
  Pass 2 is for. Do not re-attempt this by trimming; it has been tried twice.

  **The single finding worth carrying forward:** Julia's *"way too wordy — sets off my AI slop
  radar, too many adjectives and adverbs"* and Ed's *"it's a lot of text"* were the **same defect
  with one cause** — the page narrated SFV in the third person while being written by SFV. Every
  fact about the family had to be routed through an anonymizing construction (*"the group's own
  reading of that now, having thought about it a great deal, is…"*), and those constructions were
  the adjectives. Julia had independently proposed the fix without naming it: *"Ex.: 'This is our
  family, and we would like to know…'"* — which is now the hero's closing sentence nearly verbatim.

  **What Julia reacted to, recorded as evidence rather than as a change list** — her review was the
  first from anyone reading this as a reader rather than an author:

  | She said | What it turned out to indicate |
  |---|---|
  | Liked the nav bar, the *"Four relatives…"* opener, *"What it will not become"*, and the ask's different color | All kept |
  | *"Descriptive sentence under it needs refinement"* | The hero switched person mid-paragraph — "they… we". A real defect, not a style note |
  | Named the heading *"What this could be"* while quoting the H2 *"What we want this to become"* | The nav label and the heading disagreed. Both now read **"What we hope this becomes"** — her preferred register, aspirational and humble |
  | *"'What we are actually short of is not interest. It is a second family.' I don't understand this"* | The line was also **false** — `vision.md` says plainly that whether anybody wants this is unknown, since no family outside SFV has ever been asked. Deleted, not reworded |
  | *"'What else we not know…' I don't understand this"* | The "else" referred back to a sentence three paragraphs earlier. Now **"What we still do not know"** |
  | *"Enough to try one thing — YEP, that's the heart of this message"* + *"Do or do not. There is no try. —Yoda"* | Kept as the heart; retitled **"Enough to start"**, which is unambiguously a statement and drops "try" |
  | *"Maybe something other than black"* for the ask | Now deep navy, with the footer following |
  | *"I can help with that"* (on concision) | **Take her up on it.** A shorter page in her own voice is a better use of her than arguing adjectives |

  **Also fixed:** "Three things that are easy to get wrong" listed four (the two "expect…" items are
  now merged); the founding blockquote ran the full 62rem because it sat outside `.measure`
  (`blockquote` now carries `max-width` globally); `-webkit-backdrop-filter` added for Safari and
  iOS, which is the likely browser for a link arriving by text message.

  **Added from the 2026-08-26/27 timeline revisions**, all grade A: Derek's *"I hate meetings. but I
  look forward to FV meetings…"* — the most human sentence in the corpus and the page's first answer
  to *why family*; the first Demo Day being a week late because Derek was sick; the annual themes
  (*No Excuses!*, *Align!*); and the fact that the cadence was **checked against the archive rather
  than remembered**, phrased as "the longest we ever went without a Heartbeat was three weeks" to
  respect the no-cumulative-counts rule.

  **Seven GitHub links removed** — see § The repository is not the publication.

- **2026-08-25** — Built. Single page, four sections, verified at three widths. Nothing about the
  page's factual claims has needed changing since, including through the 2026-08-26 timeline
  corrections — a consequence of the no-cumulative-counts rule rather than luck.
