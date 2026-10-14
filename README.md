# Pigeon Flap (PHY 199)

A Flappy Bird–style game for PHY 199. Single-file HTML canvas game; tap, click or press Space to flap.

## Files
- `game.src.html` – the game source (edit this).
- `build.py` – `python3 build.py` writes the single-file `index.html`, embedding `audio/B.mp3`, `audio/D.mp3`, `audio/E.mp3` and `sprites/bird.png` (if present).
- `tests/logic.test.js` – `node --test` (55 tests).
- `PLAN.md` – full plan, tests table, decisions log.
- Originals (untouched): five WAVs, `pigeon.png`, `Pigeon-*.piskel`, `FlappyBirdDoc.rtf`.

## Locked decisions
**Music (class vote, Oct 14, 2026)**
| Role | Track |
|------|-------|
| Title / intro | B – Liam Obrien (`FlappyBird-LiamObrien-B.wav`) |
| Playing | E – Flying (`FlappyBird-Flying-E.wav`) |
| Game over | D – GameOver (`FlappyBird-GameOver-D.wav`) |

The play track (E) speeds up with game speed, up to `musicRateMax` (1.08x) at max speed.

Not used: A (Angelica Aguila) and C (Intro). Set in `AUDIO_ROLES` in `game.src.html`; built into `build.py` as `FINAL_TRACKS = 'BDE'`.

**Gameplay and tech**
- Collision ends the run (no penalty-and-continue); +1 per pipe pair.
- Internal resolution 144x256, scaled up pixelated. Bird 16x16, pipes 24 px wide, ground 16 px tall.
- Palette: PICO-8 (16 colors).
- Local top 10 with 3 initials (localStorage). Keys: Space/Up flap, M mute, P pause, C clear scores.
- Hosting: GitHub Pages. Tools: Piskel (sprites), jsfxr (sound effects).

## Still open
- Art: co-designed in Piskel (see the art handoff in `PLAN.md`, section 13).
- Sound effects: co-designed in jsfxr (flap, score, death). Placeholder beeps until then.
- Testing on a real phone and in Safari/Firefox.
# FlappyBird
