# TASK TO-DO — WC2026 Prediction Tracker

> This file is the single source of truth for all features, upgrades, and fixes.
> Updated every session. Survives conversation compaction.

---

## SCHEDULED

| # | Task | Status | Date | Notes |
|---|------|--------|------|-------|
| S1 | Auto-push code to GitHub | Scheduled | June 11, 6:00 AM ET | Scheduled task "game-day-push" created. Pushes all pending changes including streak claim button. |

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

**Status: BUILT — Pending push (scheduled June 11, 6 AM ET)**
**Target: Build before/on June 11**

### 1A. Signup Cutoff System (Cutoff: June 12, 12:00 AM ET)

| # | Component | Status | Description |
|---|-----------|--------|-------------|
| U1.1 | Login page cutoff warning | Built | Red banner with clock icon: "Signups close June 12, 12:00 AM ET" |
| U1.2 | First-login urgency popup | Built | Full overlay: megaphone, spinning soccer ball, live countdown, sparkles, copy-link button. Shows once per device (localStorage). "Hurry! Join the prediction game!" |
| U1.3 | Dashboard FAB invite button | Built | Pulsing soccer ball in bottom-right corner. Opens popup with share link + copy button. Visible until cutoff. |
| U1.4 | Signups closed login state | Built | Lock icon + "Signups are closed" + "Existing players can still log in" |
| U1.5 | New player rejection popup | Built | Overlay: "Signups have closed" with explanation. Blocks new names after cutoff. |
| U1.6 | Remove FAB after cutoff | Built | Floating invite button disappears after June 12 00:00 ET |

### 1B. Favourite Team & Flags

| # | Component | Status | Description |
|---|-----------|--------|-------------|
| U1.7 | Team picker modal (new players) | Built | After entering name at signup, searchable grid of all 48 WC teams. Saves to `wc2026/players/{name}/team` in Firebase. |
| U1.8 | Team picker modal (existing players) | Built | One-time "Welcome back!" popup on login if no team set. Has "Skip for now" option. Never shows again once picked. |
| U1.9 | Flags on match cards (Predict tab) | Built | Flag images from `flagcdn.com` next to team names on all match cards. |
| U1.10 | Flags on leaderboard | Built | Player's favourite team flag shown next to name in leaderboard/standings. |
| U1.11 | Flags on knockout bracket | Built | Flags next to team names in all knockout round views. |
| U1.12 | Flags across all views | Built | Results, hero dashboard, "who picked what", player profiles, etc. |

### 1C. Berry's Telegram

| # | Component | Status | Description |
|---|-----------|--------|-------------|
| U1.13 | Berry Telegram card on dashboard | Built | Inline card below leaderboard: berry emoji, "Join Berry on Telegram", links to https://t.me/BERRYNWA1. Betting tips & community. |

### 1D. Head-to-Head Player Comparison

| # | Component | Status | Description |
|---|-----------|--------|-------------|
| U1.14 | H2H comparison view | Built | Select two players, see side-by-side stats: points, exact scores, wins/draws/losses on same matches. |

### 1E. Achievement Badges

| # | Component | Status | Description |
|---|-----------|--------|-------------|
| U1.15 | Badge system | Built | Unlockable badges: First Blood (1st exact), On Fire (5-day streak), Oracle (10 exacts), plus hidden/locked badges. Shown on profile and leaderboard. |

### 1F. "Who Picked What" Pre-Match

| # | Component | Status | Description |
|---|-----------|--------|-------------|
| U1.16 | Pre-match prediction summary | Built | Before kickoff, shows all players' predictions for upcoming match. Visible after predictions lock. |

### 1G. Today's Matches Pinned Section

| # | Component | Status | Description |
|---|-----------|--------|-------------|
| U1.17 | Today's matches on dashboard | Built | Pinned section at top of dashboard showing today's matches with live indicator (pulsing red dot), scores, and kick-off times. |

### 1H. Live Match Pulse

| # | Component | Status | Description |
|---|-----------|--------|-------------|
| U1.18 | Live match indicator | Built | Pulsing red dot + glowing border on hero for matches currently in progress. |

### 1I. Animated Confetti on Exact Score

| # | Component | Status | Description |
|---|-----------|--------|-------------|
| U1.19 | Confetti celebration | Built | Falling coloured dots animation when a player nails an exact score prediction. |

### 1J. Auto-Lock Predictions

| # | Component | Status | Description |
|---|-----------|--------|-------------|
| U1.20 | Auto-lock 5 min before kickoff | Built | Prediction inputs disabled 5 minutes before match kickoff. Lock icon shown. |

### 1K. Bulk Result Entry (Admin)

| # | Component | Status | Description |
|---|-----------|--------|-------------|
| U1.21 | Bulk result entry | Built | Admin can enter multiple match results at once with "Save all results" button. |

### 1L. Match Day Summary

| # | Component | Status | Description |
|---|-----------|--------|-------------|
| U1.22 | End-of-day recap | Built | Shows points gained per player, position changes (arrows up/down), daily winners. |

### 1M. Export Leaderboard

| # | Component | Status | Description |
|---|-----------|--------|-------------|
| U1.23 | Export as shareable image | Built | Canvas-to-image export of leaderboard with download and share buttons. Includes site URL watermark. |

### 1N. Player Profile Cards

| # | Component | Status | Description |
|---|-----------|--------|-------------|
| U1.24 | Profile cards | Built | View individual player: points, exact scores, accuracy %, rank, favourite team flag, badges, join date, streak info. |

### 1O. Weekly Mini-Leagues / Side Bets

| # | Component | Status | Description |
|---|-----------|--------|-------------|
| U1.25 | Weekly mini-leagues | Built | Sub-competitions within the group. Weekly leaderboard resets each Monday, tracks best performer per week. Visual mockup done. |

### 1P. Telegram & Discord Bot Notifications

| # | Component | Status | Description |
|---|-----------|--------|-------------|
| U1.26 | Bot notifications | Placeholder | Push notifications for results, standings changes, match reminders. Berry's channel: https://t.me/BERRYNWA1 |

### 1Q. Dark/Light Theme Toggle

| # | Component | Status | Description |
|---|-----------|--------|-------------|
| U1.27 | Theme toggle | Built | Sun/moon toggle in header. Dark (current default) vs light mode. Saves preference in localStorage. Visual mockup done. |

### 1R. Prizes / Surprises for Top 3

| # | Component | Status | Description |
|---|-----------|--------|-------------|
| U1.28 | Prize podium | Built | Podium display with gold/silver/bronze after tournament ends. Prizes revealed after the final match. Visual mockup done. |

---

## TECHNICAL NOTES

- **App**: Single-file HTML at `C:\Users\oghen\Desktop\wc2026-predictions\index.html` (~2718 lines)
- **Hosting**: GitHub Pages at https://tsowho.github.io/wc2026-predictions
- **Database**: Firebase Realtime Database (compat SDK v10.12.0)
- **Admin**: `const ADMIN = "Baba";` password: `"2026*"`
- **Scoring**: 3 pts exact, 1 pt correct result, 0 wrong | Bonus: 5 pts each (6 categories) | Knockout: same scoring | Streak: 1 pt/day (manual claim), strict reset, added after final match
- **Times**: All in ET (UTC-4)
- **Editing**: Use Python scripts via bash for complex edits (Edit tool truncates large files)
- **Unpushed changes**: Streak claim button + ALL Upgrade 1 features (1A-1R) (auto-push scheduled June 11)

---

*Last updated: June 10, 2026 — Session 4 (all upgrades built)*
