# GOAT League University

A gamified educational card system for exploring football history and casting informed GOAT votes.

## Concept

Collect historical cards → build knowledge → earn FKS → vote with weight.

Your vote isn't just an opinion — it carries a score determined by how much you've learned. Study more players, unlock more categories, and increase your influence on the global rankings.

---

## Structure

```
football-gacha/
├── index.html          — Home hub
├── collection.html     — Gacha pull + card browser
├── vote.html           — GOAT voting system
├── leaderboard.html    — Live rankings
├── profile.html        — FKS profile + stats
│
├── css/
│   ├── style.css       — Design system + layout
│   ├── cards.css       — Card-specific styles
│   └── animations.css  — Pull reveals + transitions
│
├── js/
│   ├── storage.js      — All localStorage logic
│   ├── fks.js          — Knowledge Score system
│   ├── gacha.js        — Pull engine + pity system
│   ├── antiCheat.js    — Integrity checks
│   ├── app.js          — Data loader + global state
│   └── ui.js           — Shared UI helpers
│
├── data/
│   ├── players.json    — 10 handcrafted players
│   ├── cards.json      — 100 handcrafted cards
│   └── categories.json — 8 voting categories
│
└── manifest.json
```

---

## MVP Players (10)

| Player | Era | Nationality |
|--------|-----|-------------|
| Pelé | 1956–1977 | Brazil |
| Diego Maradona | 1976–1997 | Argentina |
| Johan Cruyff | 1964–1984 | Netherlands |
| Franz Beckenbauer | 1964–1983 | Germany |
| Zinedine Zidane | 1989–2006 | France |
| Ronaldinho | 1998–2015 | Brazil |
| Ronaldo Nazário | 1993–2011 | Brazil |
| Lionel Messi | 2004–present | Argentina |
| Cristiano Ronaldo | 2002–present | Portugal |
| Andrés Iniesta | 2002–2023 | Spain |

---

## Voting Categories (8)

1. **Overall GOAT** — The big debate
2. **Attacker GOAT** — Forwards & wingers
3. **Midfielder GOAT** — Central creativity
4. **Defender GOAT** — Defensive greats
5. **Best Big Match Player** — Finals & decisive moments
6. **Most Technical** — Pure skill
7. **Best Leader** — Elevating those around them
8. **Most Influential** — Changed football forever

---

## FKS System

| Action | Points |
|--------|--------|
| New card pulled | +1 |
| Card story read | +3 |
| Trivia correct | +10 |
| Trivia attempted | +1 |
| Timeline complete | +25 |
| Rivalry unlocked | +20 |
| Full set collected | +35 |

### Knowledge Levels

| Level | Range |
|-------|-------|
| Rookie Fan | 0–49 |
| Enthusiast | 50–199 |
| Historian | 200–499 |
| Tactical Analyst | 500–999 |
| Football Sage | 1000+ |

---

## Vote Weight

Your vote weight = FKS × breadth multiplier.

| Players Collected | Multiplier |
|-------------------|-----------|
| 1–2 | 30% |
| 3–4 | 60% |
| 5–6 | 80% |
| 7+ | 100% |

This prevents fanboy manipulation — you need broad knowledge to carry full influence.

---

## Deploy

Pure HTML/CSS/JS — no build step required.

**GitHub Pages:** Push to any repo, enable Pages, done.

**Local:** Open `index.html` in a browser. Note: JSON data files require a local server due to CORS.

```bash
# Python
python3 -m http.server 8080

# Node
npx serve .
```

---

## Expanding

To add more players:
1. Add entry to `data/players.json`
2. Add 10 cards to `data/cards.json` (follow existing schema)
3. Add player ID to relevant categories in `data/categories.json`

That's it. No code changes needed.

---

## Licensing

This project uses a split licence. They cover different things.

**Code** — all `.html`, `.css`, and `.js` files are released under the
[MIT Licence](LICENSE). You are free to use, modify, and distribute them,
including commercially.

**Content** — all files in `/data` (player bios, card stories, trivia,
historical analysis) are copyright © 2025 GOAT League University Contributors,
all rights reserved. Educational and non-commercial use is permitted with
attribution. Commercial use requires explicit written permission. See
[CONTENT_LICENSE.md](CONTENT_LICENSE.md) for full terms.

**Player images** — this repository contains no player photographs or
likenesses. Any fork that adds real player images must independently secure
appropriate rights. See [CONTENT_LICENSE.md](CONTENT_LICENSE.md).

---

## Disclaimer

This is an independent educational fan project. It is not affiliated with,
endorsed by, or connected to FIFA, UEFA, any national football federation, any
football club, or any player or their representatives.

All biographical and historical content is based on publicly available
information and is presented for educational and entertainment purposes only.
GOAT rankings and voting results represent community opinion, not editorial
fact or official standings.

---

## Contributing

Please read [CONTRIBUTING.md](CONTRIBUTING.md) before opening a pull request.
The bar for content contributions is intentionally high.
