# Math Maze Adventures — Classic Maze & Trailblazer Maze

A standalone, offline-friendly math adventure for the Naches Learning Hub. Two ways to explore, one game and one saved player profile system. Designed for school Chromebooks, desktop browsers, and touchscreens.

## Play modes

### Classic Maze — original game, improved readability

The original worksheet-style maze is preserved: solve the current room's math question, then choose the exit bearing the correct answer. Correct answers move you along the generated route. You can select any of three **visibility modes**:

- **Standard:** Complete maze visible, with inactive rooms dimmed and valid exits enlarged.
- **Focus:** Zooms into the current room and nearby exits for easier reading.
- **High Contrast:** Highlights the current room and exit choices while further reducing background distractions.

The large answer buttons and number-key shortcuts (1–4) are retained. Existing Classic records and locally stored matches remain compatible.

### Trailblazer Maze — new direction-first gameplay

1. Choose one of the **connected** corridors displayed on the board or in the movement panel.
2. The game reveals a new math question **after** you choose the direction.
3. Solve it by selecting one of four answers **or** typing your answer (configured before starting).
4. A correct answer moves you into the next room; an incorrect answer sends you back **one previously visited room** and clears the question. From the starting room you stay put.
5. Travel from **START** (bottom-right) to the goal at the top-left. Your progress is preserved automatically when browser storage is available.

Movement supports all **eight directions** when passages permit. A diagonal option is gold/dashed, takes a shorter route, and asks a slightly more advanced question when grade/skill allows. Diagonals only appear when there is an unblocked two-edge corner route; they never pass through a wall.

If you leave surprise rooms on, roughly 10% of interior rooms hide bonus cards and 10% hide traps (the actual count is rounded for maze size). Each surprise triggers **only once per maze**. Possible bonuses include score rewards and a shield to prevent one wrong-answer setback. Traps can deduct bonus points or send you back a room. Disable surprises during game setup to focus entirely on math.

## Game settings

- **Adventure:** Classic Maze or Trailblazer Maze.
- **Grade:** 1–12; skill selection updates to match the grade.
- **Skills:** Addition, subtraction, multiplication, division, fractions, decimals, area/perimeter, percentages, integers, algebra, exponents and more, depending on grade.
- **Maze:** 4×4, 5×5 or 6×6.
- **Themes:** Bee Garden, Star Quest, Treasure Ruins.
- **Difficulty pacing:** Practice (unlimited attempts), Challenge (three mistakes), Speed Run (timed, three mistakes).
- **Trailblazer answers:** Four-choice multiple choice or typed answers, including fractions like `2/3`, decimals, and negative numbers.
- **Surprise rooms:** On or off.
- **Visibility:** Standard, Focus, High Contrast (can switch during play).

Typed answers recognize mathematically equivalent fractions such as `2/4` for `1/2`.

## Saved progress

The game deliberately **retains the original localStorage key** `naches_math_maze_v1`. No account is needed. Existing Classic player nicknames, wins, achievements, and available saved matches are read using their original format. Both modes contribute to the existing achievement milestones, and best scores are recorded separately per adventure and difficulty. Browser storage is device-and-browser specific; students switching devices will not automatically share records. Private/incognito mode or clearing browser data can erase local progress.

**Important:** An unfinished match is stored in one session slot per active game/profile workflow. Starting a new maze replaces the previous unfinished maze. Do not clear site storage before checking saved progress.

## Deploy to GitHub Pages

**Use the same existing repository:** `math-maze-adventures`.

1. Download the **GitHub Ready** ZIP.
2. Extract `index.html` and `README.md`.
3. Open the existing Math Maze Adventures GitHub repository.
4. Replace those two files in the **root of the `main` branch**; do not put them in a subfolder.
5. Confirm **Settings → Pages → Deploy from a branch → `main` → `/(root)`** is enabled.
6. Open the existing game URL, refresh with Ctrl+Shift+R, and verify both modes.

There are no external libraries, fonts, APIs, accounts, or assets. The page runs from a single `index.html`. You **do not** need to update the main Learning Hub repository because the game URL stays unchanged.

## Quick teacher smoke test

1. Open Classic Maze, try an answer, and switch Standard → Focus → High Contrast.
2. Start Trailblazer Maze, choose a diagonal corridor when available, and verify the question appears **after** choosing the direction.
3. Try a wrong answer: the token should retreat one room and the next direction should generate a fresh question.
4. Try a correct typed answer (including fractions when a fraction question appears).
5. Enable surprise rooms, trigger a bonus or trap, and dismiss its card.
6. Refresh during an open Trailblazer question and confirm **Resume** restores it (on a normal hosted site, not an incognito/private session).
7. Verify that a previously saved Classic profile still shows its records.

## Status & validation

Development build: **Math Maze Adventures 2.0**, featuring a new *Trailblazer Maze* mode (the mode itself is intentionally not named "2.0"). In headless Chromium, testing covered 5 Classic route simulations, 27 complete Trailblazer runs across 4×4/5×5/6×6, 1,000+ allowed diagonals checked against wall rules, desktop/tablet/mobile layouts, typed and multiple-choice answers, wrong-answer setbacks, event cards, legacy Classic sessions, and simulated saving mid-question. Tests passed without JavaScript exceptions.

Still recommended before a wide classroom rollout: live GitHub Pages save/resume, physical Chromebook/touchscreen interaction, and teacher review of grade-appropriate diagonal difficulty.

## Files

- `index.html`: Complete playable game and inline code/styles.
- `README.md`: Repository documentation (this document).
- In the optional complete package: preview screenshots, browser test scripts/results, deployment notes.
