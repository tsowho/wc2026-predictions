# TASK TO-DO — WC2026 Prediction Tracker

> This file is the single source of truth for all features, upgrades, and fixes.
> Updated every session. Survives conversation compaction.

---

## SCHEDULED

| # | Task | Status | Date | Notes |
|---|------|--------|------|-------|
| S1 | Auto-push code to GitHub | ~~Scheduled~~ No longer needed | June 11, 6:00 AM ET | Was scheduled but user pushed manually on June 10. |

---

## COMPLETED

| # | Feature | Date Completed |
|---|---------|----------------|
| C1 | Football pitch hero background | June 9 |
| C2 | Burning fuse countdown animation | June 9 |
| C3 | Mystery gift + cauldron streak teaser (pre-tournament) | June 9 |
| C4 | Trash talk merged into hero ticker | June 9 |
| C5 | Animation reset fix (data-hash memoization) | June 9 |
| C6 | Chat section (Firebase-synced, bubble style) | June 9 |
| C7 | Knockout stage tab (R32 through Final) | June 9 |
| C8 | Collapsible bonus predictions | June 9 |
| C9 | Default predict tab to Group A | June 9 |
| C10 | Hide played matches from predict tab | June 9 |
| C11 | Group tooltips on hover | June 9 |
| C12 | Glass-style login box with countdown, player count, 104 matches badge | June 9 |
| C13 | Streak claim button (manual press, no auto-record) | June 10 |

---

## UPGRADE 1 — Game Day Mega Update

**Status: BUILT & PUSHED TO GITHUB**
**Pushed: June 10, 2026**
**Live at: https://tsowho.github.io/wc2026-predictions**

### 1A. Signup Cutoff System (Cutoff: June 12, 12:00 AM ET)

| # | Component | Status | Description |
|---|-----------|--------|-------------|
| U1.1 | Login page cutoff warning | Done | Red banner with clock icon: "Signups close June 12, 12:00 AM ET" |
| U1.2 | First-login urgency popup | Done | Full overlay: megaphone, spinning soccer ball, live countdown, copy-link button. Shows once per device (localStorage). |
| U1.3 | Dashboard FAB invite button | Done | Pulsing soccer ball in bottom-right corner. Opens popup with share link + copy button. Visible until cutoff. |
| U1.4 | Signups closed login state | Done | Lock icon + "Signups are closed" + "Existing players can still log in" |
| U1.5 | New player rejection popup | Done | Overlay: "Signups have closed". Blocks new names after cutoff. |
| U1.6 | Remove FAB after cutoff | Done | Floating invite button disappears after June 12 00:00 ET |

### 1B. Favourite Team & Flags

| # | Component | Status | Description |
|---|-----------|--------|-------------|
| U1.7 | Team picker modal (new players) | Done | Searchable grid of all 48 WC teams. Saves to `wc2026/playerTeams/{name}` in Firebase. |
| U1.8 | Team picker modal (existing players) | Done | "Welcome back!" popup on login if no team set. "Skip for now" option. |
| U1.9 | Pick/Change team button on dashboard | Done | Top-left of dashboard. Opens team picker anytime. |
| U1.10 | Flags on all match cards | Done | Flags via `flagcdn.com` on Predict, Results, Live, Dashboard, Knockout tabs. |
| U1.11 | Flags on leaderboard | Done | Player's favourite team flag next to name. |
| U1.12 | Flags on Players tab | Done | Favourite team flag next to each player name. |

### 1C. Berry's Telegram

| # | Component | Status | Description |
|---|-----------|--------|-------------|
| U1.13 | Berry Telegram card on dashboard | Done | Card at bottom of dashboard linking to https://t.me/BERRYNWA1 |

### 1D. Head-to-Head Player Comparison

| # | Component | Status | Description |
|---|-----------|--------|-------------|
| U1.14 | H2H comparison view | Done | On Leaderboard tab: select two players, see side-by-side stats. |

### 1E. Achievement Badges

| # | Component | Status | Description |
|---|-----------|--------|-------------|
| U1.15 | Badge system | Done | First Blood, On Fire, Oracle, Sharpshooter, Hot Streak. Shown on leaderboard and profiles. |

### 1F. "Who Picked What"

| # | Component | Status | Description |
|---|-----------|--------|-------------|
| U1.16 | Post-kickoff prediction summary | Done | Shows all players' predictions after match starts. |

### 1G. Today's Matches Pinned Section

| # | Component | Status | Description |
|---|-----------|--------|-------------|
| U1.17 | Today's matches on dashboard | Done | Pinned at top with live dots, scores, kick-off times. |

### 1H. Live Match Pulse

| # | Component | Status | Description |
|---|-----------|--------|-------------|
| U1.18 | Live match indicator | Done | Pulsing red dot on today's matches and live tab. |

### 1I. Animated Confetti on Exact Score

| # | Component | Status | Description |
|---|-----------|--------|-------------|
| U1.19 | Confetti celebration | Done | Canvas animation fires when player gets exact score. |

### 1J. Auto-Lock Predictions

| # | Component | Status | Description |
|---|-----------|--------|-------------|
| U1.20 | Auto-lock 5 min before kickoff | Done | `isAutoLocked()` function disables inputs 5 min before match. |

### 1K. Bulk Result Entry (Admin)

| # | Component | Status | Description |
|---|-----------|--------|-------------|
| U1.21 | Bulk result entry | Done | Admin dashboard section: enter multiple scores, "Save all results" button. |

### 1L. Match Day Summary

| # | Component | Status | Description |
|---|-----------|--------|-------------|
| U1.22 | End-of-day recap | Done | Daily points per player on dashboard. |

### 1M. Export Leaderboard

| # | Component | Status | Description |
|---|-----------|--------|-------------|
| U1.23 | Export as PNG image | Done | Canvas export on Leaderboard tab with site URL watermark. |

### 1N. Player Profile Cards

| # | Component | Status | Description |
|---|-----------|--------|-------------|
| U1.24 | Profile cards | Done | Click player on Leaderboard: points, exact scores, accuracy %, rank, badges, team flag, streak. |

### 1O. Weekly Mini-Leagues

| # | Component | Status | Description |
|---|-----------|--------|-------------|
| U1.25 | Weekly mini-leagues | Done | Monday–Sunday leaderboard on dashboard. |

### 1P. Telegram & Discord Bot Notifications

| # | Component | Status | Description |
|---|-----------|--------|-------------|
| U1.26 | Bot notifications | Placeholder | Requires server-side setup. Not feasible in client-only app. |

### 1Q. Dark/Light Theme Toggle

| # | Component | Status | Description |
|---|-----------|--------|-------------|
| U1.27 | Theme toggle | Done | Sun/moon button on dashboard top-right. CSS `[data-theme]` overrides. Saves to localStorage. |

### 1R. Prizes / Surprises for Top 3

| # | Component | Status | Description |
|---|-----------|--------|-------------|
| U1.28 | Prize podium | Done | Gold/silver/bronze podium appears on dashboard after tournament ends (`WC_END`). |

---

## HOTFIXES (Post-Upgrade 1)

| # | Fix | Date | Description |
|---|-----|------|-------------|
| H1 | Theme toggle CSS rules | June 10 | Added `[data-theme="light"]` and `[data-theme="dark"]` CSS variable overrides. Toggle was setting attribute but no CSS responded to it. |
| H2 | Theme toggle moved to dashboard | June 10 | Was on Leaderboard tab, user wanted it on main dashboard. |
| H3 | Pick/Change team button | June 10 | Added dashboard button so players who skipped team picker can select later. |
| H4 | Flags everywhere | June 10 | Added `teamFlag()` calls to all render functions: dashboard next match, live cards, predict cards, results cards, knockout bracket, players list. 28 total flag insertions. |

---

## CURRENT STATE

- **All Upgrade 1 features (1A–1R): DONE** (27/28 built, 1 placeholder)
- **App size**: ~2720 lines, single-file HTML
- **Last push**: June 10, 2026 (manual push by user via Git Bash)
- **Pending pushes**: H1–H4 hotfixes (theme fix + flags everywhere) — command in clipboard, awaiting user paste in Git Bash

---

## TECHNICAL NOTES

- **App**: Single-file HTML at `C:\Users\oghen\Desktop\wc2026-predictions\index.html`
- **Hosting**: GitHub Pages at https://tsowho.github.io/wc2026-predictions
- **Database**: Firebase Realtime Database (compat SDK v10.12.0)
- **Firebase paths**: `wc2026/players`, `wc2026/predictions`, `wc2026/actuals`, `wc2026/bonus`, `wc2026/bonusActuals`, `wc2026/loginDates`, `wc2026/chat`, `wc2026/passwords`, `wc2026/joinTimes`, `wc2026/reactions`, `wc2026/knockout/*`, `wc2026/playerTeams`
- **Admin**: `const ADMIN = "Baba";` password: `"2026*"`
- **Scoring**: 3 pts exact, 1 pt correct result, 0 wrong | Bonus: 5 pts each (6 categories) | Knockout: same scoring | Streak: 1 pt/day (manual claim), strict reset, added after final match
- **Times**: All in ET (UTC-4)
- **Signup cutoff**: June 12, 12:00 AM ET = `new Date('2026-06-12T04:00:00Z')`
- **Flags**: `flagcdn.com` CDN, country codes in `TEAM_FLAGS` constant
- **Editing**: Use Python scripts via bash for complex edits (Edit tool truncates large files)

---

*Last updated: June 10, 2026 — Session 4 (all upgrades built & pushed, hotfixes pending)*
