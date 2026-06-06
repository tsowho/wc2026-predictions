# World Cup 2026 Prediction Tracker

A free, interactive web app for tracking FIFA World Cup 2026 score predictions with your friends.

**Live site:** [https://tsowho.github.io/wc2026-predictions](https://tsowho.github.io/wc2026-predictions)

## Features

- All 72 group stage matches with real dates, times (ET), and venues
- All 48 teams across 12 groups from the official FIFA draw
- Simple scoring: 3 pts for exact score, 1 pt for correct result, 0 for wrong
- Live leaderboard with accuracy stats per player
- Dashboard with countdown to next match
- Filter matches by group (A–L)
- Export/import data as JSON for backup or sharing
- Dark mode (auto-detects system preference)
- Works on desktop and mobile — no server needed

## How to use

1. Open the app and go to the **Players** tab
2. Add everyone in your prediction group
3. Each person selects their name in the **Predict** tab and enters their score predictions before each match
4. After a match finishes, go to the **Results** tab and enter the actual score
5. Check the **Leaderboard** to see who's winning

## How to share with your group

**Option A — Share the link:** Send the GitHub Pages link above. Each person's data saves in their own browser. One person acts as admin, collecting exported JSON files and importing them into the master copy.

**Option B — Send the file:** Download `index.html` and send it via WhatsApp, email, or any messenger. Works offline.

## Roadmap

- [ ] Knockout stage matches (Round of 32 through Final)
- [ ] Shared backend (Firebase) for real-time multiplayer sync
- [ ] Telegram bot integration
- [ ] Discord bot integration
- [ ] Bonus predictions (tournament winner, golden boot)

## License

MIT
