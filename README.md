# Faint.

**The daily color-perception game.** One tile is a *faintly* different shade than
the rest. Find it. Every round it gets harder — the grid grows and the difference
shrinks — until your eyes give out.

👉 **Play:** https://rahulatrkm.github.io/faint/

- 🎯 **A new puzzle every day** — deterministic seed, so everyone plays the same
  daily challenge
- 📈 **Escalating difficulty** — 3×3 up to 9×9, color difference shrinking to the
  edge of human perception
- ❤️ **3 lives**, a per-round timer, and a score = how many rounds you cleared
- 📊 **Wordle-style shareable result** — an emoji grid of how you did:

  ```
  Faint #143 — Round 17
  🟩🟩🟩🟨🟩
  🟩🟨🟩🟩🟨
  🟩🟩🟩⬛
  ```

- 🔥 **Streaks & best score** kept locally
- 🕹️ **Endless mode** for "just one more"

## Why it's nice

- **Nothing to install, no account, no tracking, no ads.** One static
  `index.html`.
- **Works offline** and on mobile (touch-friendly).
- **Open source** — read the whole thing, it's ~1 file of vanilla JS.

## How the difficulty works

Each round picks a pleasant random base color (HSL) and nudges one tile's
lightness/hue by a shrinking perceptual delta (starts ~26 units, floors ~2.2).
The grid grows every couple of rounds. A miss retries the same difficulty and
costs a life; clear it and it steps up.

## Run locally

```bash
python3 -m http.server 8000   # then open http://localhost:8000
```

## License

MIT.
