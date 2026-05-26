# Contributing

Thank you for your interest in contributing to GOAT League University.

Before opening a pull request, please read this document in full — especially
the content section. Contributions that don't meet these standards will be
closed without merging.

---

## Two types of contribution

This project has a clear split: **code** (MIT licensed) and **content**
(copyright, all rights reserved). Different rules apply.

---

## Code contributions (HTML / CSS / JS)

These are welcome. Good targets:

- Bug fixes
- Accessibility improvements
- Performance improvements
- Mobile layout fixes
- New UI features that don't require new content

**Rules:**
- One concern per PR. Don't fix a bug and redesign a component in the same PR.
- No new dependencies. This project is intentionally dependency-free.
- No build tools. It must remain deployable by dragging a folder to GitHub Pages.
- No player images. See the image policy below.

---

## Content contributions (`/data` files)

These are accepted selectively. The bar is high, deliberately.

### Adding a new player

A new player entry requires all of the following or it won't be merged:

- A complete `players.json` entry with all fields populated
- Exactly **10 cards** in `cards.json`, each with:
  - An original, handcrafted `story` (minimum 80 words, not paraphrased from
    Wikipedia)
  - An original `historicalSignificance` (minimum 40 words)
  - A factually verified `triviaQuestion` with exactly 4 options and a correct
    answer index
  - Appropriate `rarity` assignment (not everything can be legendary)
  - Correct `era` labels (Youth / Rise / Prime / Legacy)
- The player added to at least one category in `categories.json` with a
  justified `minFKS` threshold

**Do not submit players you cannot fully research.** A shallow entry with
generic stories is worse than no entry. We will close PRs that contain
templated or AI-generated content that hasn't been verified against sources.

### Fixing factual errors

These are the most valuable contributions. If a card contains an inaccuracy —
a wrong year, a misattributed quote, a disputed statistic — open an issue
first describing the error and your source, then submit a PR.

### Trivia questions

All trivia must be:
- Verifiable against at least one reputable source
- Unambiguous — there must be exactly one correct answer
- Appropriate for the card's era and theme
- Not duplicated across cards

---

## What will not be merged

- Player images of any kind (photographs, illustrations, likenesses)
- Content about living players that is speculative, opinionated, or
  unverifiable
- New voting categories without a clear justification and eligible player list
- Dependencies, build steps, or backend requirements
- Anything that requires a server to function — this project must remain
  static
- AI-generated content submitted without human verification of every fact

---

## Image policy

This repository will not accept player photographs or likenesses. The reasons
are practical, not aesthetic: football image rights are held by players, clubs,
photographers, and agencies, and the cost and complexity of clearing rights for
even a small roster is prohibitive for a free educational project.

If you fork this project and add images privately, that is your responsibility
to licence correctly. Do not submit images to this repository.

---

## Copyright assignment

By submitting a pull request that modifies or adds content to the `/data`
directory, you agree that:

1. The content is your original work.
2. You are assigning copyright in that content to the GOAT League University
   project maintainers.
3. The content will be governed by `CONTENT_LICENSE.md`.

Code contributions remain under MIT.

---

## Opening an issue

Issues are welcome for:
- Factual errors in card content
- Bug reports (include browser, OS, and steps to reproduce)
- Feature proposals (discuss before building)

Issues are not the place for GOAT debates. There's a voting system for that.
