# World Cup 2026 Prediction Tracker

A free, interactive web app for tracking FIFA World Cup 2026 score predictions with your friends. Real-time multiplayer sync via Firebase — no server setup needed.

**Live site:** [https://tsowho.github.io/wc2026-predictions](https://tsowho.github.io/wc2026-predictions)

## Features

- All 72 group stage matches with real dates, times (ET), and venues
- All 48 teams across 12 groups from the official FIFA draw
- **Real-time multiplayer** — Firebase syncs predictions and results across all players instantly
- **Per-player passwords** — each player sets their own password on first join
- Simple scoring: 3 pts for exact score, 1 pt for correct result, 0 for wrong
- **Bonus predictions** — 6 categories (tournament winner, golden boot, best group team, finalists, most goals in a match) worth 5 pts each, closes after group stage
- **Chess rank system** — players earn ranks (King, Queen, Rook, Bishop, Knight, Pawn) based on leaderboard position
- **Animated hero dashboard** — live countdown ticker, mini podium, player stats, bouncing soccer ball, floating particles, rotating trash talk
- **World Cup winners background** — scrolling display of every past winner with country flag colors
- **News tab** — live World Cup headlines from Google News, auto-refreshes every 5 minutes
- **Celebrations** — streaks, achievements, position change arrows, MVP badges, confetti
- Live leaderboard with accuracy stats, bonus column, and player cards
- Filter matches by group (A–L)
- Dark mode (auto-detects system preference)
- Works on desktop and mobile
- Admin controls: enter results, reset passwords, manage players
- Admin (Baba) is hidden from other players' views

## How to use

1. Open the live site and enter your name
2. Set a password on first join (returning players log in with their password)
3. Go to the **Predict** tab — enter scores and click **Lock** before each match starts
4. Fill in **Bonus Predictions** before the group stage ends (June 27)
5. After a match finishes, the admin enters the actual score in the **Results** tab
6. Check the **Leaderboard** and **Dashboard** to see who's winning
7. Read the latest tournament news in the **News** tab

## Scoring

- **Exact score** — 3 points (e.g., you predicted 2-1 and it was 2-1)
- **Correct result** — 1 point (you got the winner/draw right but not the exact score)
- **Wrong** — 0 points
- **Bonus predictions** — 5 points each for correct picks

## Tech stack

- Single HTML file, no build tools
- Firebase Realtime Database (free tier) for multiplayer sync
- GitHub Pages hosting
- Google News RSS via rss2json.com for news feed

## Roadmap

- [x] Real-time multiplayer sync (Firebase)
- [x] Per-player passwords
- [x] Chess rank system
- [x] Animated hero dashboard
- [x] World Cup winners scrolling background
- [x] Bonus predictions (6 categories, 5 pts each)
- [x] News tab with live headlines
- [x] Celebrations, streaks, and achievements
- [ ] Knockout stage matches (Round of 32 through Final)
- [ ] Telegram bot (notifications, predict via chat, leaderboard commands)
- [ ] Discord bot (notifications, predict via chat, leaderboard commands)

## License

MIT
