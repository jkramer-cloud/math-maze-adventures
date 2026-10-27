# Math Maze Adventures — Wildlands Soundscape

A free, original, offline-friendly, browser-based educational math game for the Naches Learning Hub. One page includes **three playable modes**:

1. **Classic Maze** — solve a problem and select the matching route, with Standard, Focus, and High Contrast viewing options.
2. **Trailblazer Maze** — choose a direction (including valid diagonals) and then solve a generated question. Optional traps and bonuses, multiple-choice or typed answers.
3. **Wildlands Adventure** — explore five regional maps; challenge Mathlings and bosses, practice missed skills to heal, earn badges, and unlock explorer outfits.

## What's new in this update

### Original Wildlands soundtrack
- Five separate exploration melodies: Orchard Fields, Whispering Forest, Crystal Caverns, River Crossing, Summit Ruins.
- Different music during ordinary Mathling encounters, regional bosses, the final boss, and visits to the Practice Lodge.
- Music is original and synthesized using the browser's Web Audio API. There are **no audio files, libraries, external assets, requests, or subscriptions**.
- Audio starts **muted by default** in classrooms. Open the **Wildlands Sound Studio** beneath the game setup to enable music and effects.
- Independent music and effects volume sliders and a **Test my sound settings** button. These preferences stay in the browser.
- Music stops when switching to Classic/Trailblazer, pausing/muting the game, or hiding the tab.

### Added sound effects
Footsteps, entering an encounter, correct/incorrect answers, healing, moving between regions, defeated Mathlings, boss victory, and fainting.

### Sprite improvements
- Added original colored SVG Mathling sprites for each region, with a crown for bosses and a special Practice Lodge guide.
- Added subtle idle/bounce animation to Mathlings and step/arm movement to explorer sprites.
- Player tokens smoothly move to adjacent squares; the game honors **Reduce Motion** browser/operating-system preferences.

## How to play Wildlands
1. Open the game and select **Wildlands Adventure**.
2. Select a grade (1–12), a math-answer style (four-choice or type your answer), a starter character and color.
3. Start an adventure. Move with WASD, arrow keys, touch arrows, or click an adjacent map square.
4. Enter tall terrain to encounter a Mathling. Correct answers defeat enemies and award XP; incorrect answers cost hearts and record the missed skill.
5. Visit the **Practice Lodge** at the upper-left (or use the Return to Practice Lodge button) to answer related problems and restore hearts.
6. Defeat regional bosses to collect five badges, then attempt the Grand Summit final challenge.
7. Unlock cosmetics as your XP increases. Older Classic/Trailblazer progress stays in its original save format.

## Upload to GitHub Pages

Use your **existing `math-maze-adventures` GitHub repository**. Do not create a new repository.

1. Download and extract the `Math_Maze_Wildlands_Soundscape_GitHub.zip` package.
2. Upload **`index.html` and `README.md`** to the **root** of your existing repository, replacing the previous copies.
3. Commit the change on `main`.
4. Ensure GitHub **Settings → Pages → Deploy from a branch → `main` → `/(root)`** is selected.
5. Open your existing Math Maze Adventures URL and hard-refresh the page (**Ctrl+Shift+R**).
6. Choose Wildlands, toggle **Enable original Wildlands music & sounds**, and press **Test my sound settings**.
7. Verify Classic and Trailblazer remain usable, and check your profile saves between sessions.

**No Learning Hub edit is needed:** this updates the existing game at its existing URL.

## Privacy, performance, and accessibility
- Everything runs locally in the browser; no accounts or online score server.
- Player progress and audio settings are stored on that device using browser localStorage.
- A browser may prevent auto-playing sound until the student clicks a control; the game requires deliberate opt-in and provides a test button.
- Designed to remain usable without audio. Audio provides atmosphere, not information required to solve questions.
- Reduced-motion settings stop added animations.
- Using large numbers of simultaneously open game tabs may consume extra resources; close unused tabs.

## Testing and release status

Automated Chromium tests passed for desktop/mobile layout, Wildlands navigation, encounters, mode switching, correct-answer actions, Practice Lodge interactions, five regional music tracks, audio opt-in/mute, audio scheduling, and reduced motion. Audio was verified by tracking Web Audio events, **not through physical speaker listening**. Real-device listening, headphone balance, GitHub Pages deployment, and a sustained student classroom session remain to be checked. Consider this a **playable development update**, not a fully classroom-qualified release.

### Files
- `index.html` — the complete playable game, graphics, music, and sound engine.
- `README.md` — these instructions.
- Full package only: `TEST_RESULTS.md`, screenshots and test scripts.

This is original classroom game content; Pokémon names, monsters, sprites, and soundtrack assets are not used.
