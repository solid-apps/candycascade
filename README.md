# Candy Cascade 🍬

A match-3 game in a single HTML page, with a daily board, challenge links and an endless zen mode.

Live: https://solid-apps.github.io/candycascade/

## Features

- 8×8 board with six candy colours. Swipe or tap two neighbouring candies to swap them.
- Match 4 or more to make special candies, and combine specials for bigger effects.
- Classic mode: 15 hand-made levels where you clear the jelly (single and double) within a move limit. Some levels add ice, chocolate that spreads, and holes. After level 15 the levels repeat with double jelly and fewer moves.
- Win streak boosters: winning levels in a row puts free special candies on the next board.
- If you run out of moves with at least 85% of the jelly cleared, you are offered 5 free moves once per level.
- Daily challenge: one try a day. Everyone gets the same seeded board, which changes at midnight UTC. Each weekday has its own rule (for example Sprint Wednesday has 14 moves, Five-Colour Friday has 5 colours, Jelly Sunday has bonus jelly). You score up to three stars and build a daily streak.
- Challenge links: share a daily result as a link (`?d=<day>&beat=<score>`). Whoever opens it plays the same board and tries to beat that score, and can retry as often as they like.
- Zen mode: endless play with no move limit.
- A hint shows after 5 seconds without a move, and the board reshuffles when no moves are left.
- Sound effects and generated music made with the Web Audio API (no audio files), plus vibration on supported devices. Separate buttons turn sound and music on or off.
- Stats screen: daily games played, streaks, star counts, levels won, candies crushed, biggest cascade and best score.
- Sharing uses the Web Share API, or copies to the clipboard if that isn't available.
- Installable as a PWA. A service worker caches the app so it works offline.

## Your data

- All data stays in your browser's `localStorage`, in keys that start with `cc_`. This covers best score, highest level, daily result and streak, win streak, stats, sound and music settings, and whether the tutorial has been seen.
- The app does not use a Solid pod, and it has no sign-in. Nothing is sent to a server. Everything works without an account.
- The only data that leaves your device is what you choose to share: a score message, or a challenge link with the day number and your score.

## Run locally

The game is a static site with no build step. Serve the folder with any static server, for example:

```sh
python3 -m http.server
```

Then open http://localhost:8000/.
