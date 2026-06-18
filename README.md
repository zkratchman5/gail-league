# GAIL — The Great American Inter-League

An interactive wireframe for a 12-manager, multi-sport fantasy league spanning
10 pro sports (NFL, NBA, NHL, MLB, WNBA, PGA, ATP, WTA, EPL, UFC) plus a Team
Success lane.

## Live site

Once GitHub Pages is enabled, this is served from `index.html` at the repo's
Pages URL.

## What's here

- **`index.html`** — the entire prototype. Self-contained: HTML, CSS, and JS in
  one file, no build step, no dependencies. Open it directly in any browser.

## Core concept

Each of 11 lanes (10 sports + Team Success) ranks all 12 managers 1st–last and
converts finish to ladder points (1st = 12 down to last = 1; max 132 total).
This sidesteps the problem of normalizing scoring volume across sports.

## Sections (tabs)

- **Standings** — leader cards + a 12×11 heat-grid matrix (managers × lanes),
  sortable by any lane, expandable per manager. Toggle ladder points vs native
  score.
- **Roster** — ESPN-style stat grid per sport with per-player and starters-total
  fantasy points.
- **Scoring** — rank-ladder rules, Team Success bonus ladder, UFC model, plus a
  per-sport tab using real ESPN default scoring (NFL/NBA/NHL/MLB) and each
  platform's native format for the rest (FedExCup, ATP/WTA Race, FPL, custom UFC).
- **Auction** — mock monthly real-money auction with bid validation, cap
  tracking, and a growing prize pot.
- **Top Available** — filterable/sortable free-agent pool.
- **Draft Board** — classic snake grid (rounds × 12 managers) from the inaugural
  mixed-sport draft, with a per-sport highlight filter.

## State / limitations

All interactivity runs client-side and resets on refresh. There is no backend,
no persistence, and no cross-user sync yet — each visitor sees their own
independent session. Data is seeded sample data, not live.

## Next build-out ideas

- Real backend + database so standings, rosters, and the auction are shared and
  live across managers
- Live data feeds per sport to compute native fantasy scores automatically
- Auth for the 12 managers
- Link draft picks to roster/player pages
- Rival-roster viewer
