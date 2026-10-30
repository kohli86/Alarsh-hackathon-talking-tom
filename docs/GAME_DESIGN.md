# Game Design Document

## 1. SDG connection
**Goal 3: Ensure healthy lives and promote well-being for all.**
- **3.4** Reduce non-communicable diseases and promote mental health: healthy food, exercise, sleep, kind conversations.
- **3.3** End epidemics and fight communicable diseases: handwashing.
- **3.9** Reduce illness from unsafe water: clean-water option.

Goal: build healthy habits in children through caring for a pet, and teach one real fact per action.

## 2. Story
Mochi moves to a new village without knowing how to stay healthy. The player is Mochi's buddy for 7 days. Win: survive 7 days as a *Healthy Hero*. Lose: health ≤ 15%.

## 3. Core loop
Stats decay → player notices low stat or Mochi complains → player chooses an action → stat rises, fact appears → repeat.

## 4. Mechanics
| Stat | Decay / sec | Raised by |
|---|---|---|
| Food | -1.3 | Feed |
| Energy | -0.9 (+5 asleep) | Sleep, water |
| Clean | -1.0 | Wash |
| Fitness | -0.4 | Exercise, veggies |
| Mood | -0.6 (extra -0.8 if food/clean/energy low) | Talk, play, treats, poke |

- Health = average of 5 stats. Day length 45 s, 7 days total.
- 3 junk foods in one day = tummy ache penalty (teaches balance, treats are not banned).
- Mini-games: Scrub (10 taps), Jump (taps in 6 s, more taps = bigger gain).
- Talk: 3 replies, one supportive. Order is shuffled.
- Game pauses while a dialog is open.

## 5. Judging checklist
| Criterion | Where |
|---|---|
| Playable prototype | `index.html` (GitHub Pages) |
| Clear mechanics | Section 4 |
| Story / logic | Sections 2 and 3 |
| SDG sub-theme | Section 1 (3.3, 3.4, 3.9) |
| Repo and docs | README + this file |

## 6. Testing
Played on desktop and mobile browsers (Chrome). To change difficulty edit decay values in `tick()`.
