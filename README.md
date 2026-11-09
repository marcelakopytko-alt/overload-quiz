# Which overload are you carrying?

A five-minute self-diagnostic for UX designers, built from Laura Willis's talk
**"AI Without Exhaustion — Making Real Change, Reclaiming Focus, Boundaries, and Balance"** (30 October 2026)
and her HARMONY framework.

Live: https://marcelakopytko.github.io/overload-quiz/

## What it does

Ten statements produce a score across five overload types, each with a different fix:

| Type | Anchored in |
|---|---|
| Attention overload ("brain fry") | Her phrase: juggling multiple AI tools and work streams |
| Cognitive overload | Her answer to the audience question: focus time, fewer distractions |
| Recovery impairment | Her term: working after hours, or staying attached to work delegated to AI |
| Meeting overload | 76% attend out of obligation, 87% are distracted |
| AI dependency & skill drift | Nurture human skills, mindful use |

Then: three questions from the talk's close, and a picker for one or two of her twelve
adjustments.

## Design notes

- **Single self-contained file.** No CDN, no fonts, no analytics, no server. Works offline
  from a local file, a shared drive, or any static host.
- **Answers never leave the browser.** "Copy link to my result" puts the ten answers in the
  URL fragment (`#r=3,3,2,2,...`). Fragments are not sent to the server, so nothing is logged.
- **The taxonomy is an interpretation.** The talk names attention overload, cognitive overload
  and recovery impairment directly. Meeting overload and AI skill drift are drawn from the rest
  of her material. This is stated on the page itself and each result card cites its source.
- Not a clinical instrument.

## Files

- `index.html` — the whole thing
- `.nojekyll` — tells GitHub Pages not to run Jekyll

## Updating

Edit `index.html`, commit, push. GitHub Pages redeploys in about a minute.

If you edit the questions, keep `PAIRS` in the script in sync: it maps question numbers to
type, and each type must keep exactly two questions so scores stay on a 0–6 scale.
