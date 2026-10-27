# Math Maze Adventures — Wildlands Edition

**Three educational math games in one self-contained website** for the Naches Learning Hub. The app runs from `index.html` and stores progress locally in the browser. No logins, analytics, accounts, or external assets are required.

## Choose a game mode

A three-choice popup appears whenever the game opens.

- **Classic Maze** — Follow the corridor with the answer to the current math problem. Version 3 uses compact numbered corridor markers instead of the old large answer circles that obscured nearby math expressions. Current-room problem and large answer choices remain visible. Standard, Focus, and High Contrast views are available.
- **Trailblazer Maze** — Choose a permitted cardinal or diagonal direction first, then solve a newly generated question. Diagonals are harder, and an incorrect answer sends the explorer back one space unless a shield prevents it. Optional traps and rewards remain available.
- **Wildlands Adventure** — Walk through a top-down world with WASD, arrow keys, the on-screen direction pad, or by clicking an adjacent tile. Tall terrain can spawn a Mathling challenge. Correct answers reduce its shields; incorrect answers cost a heart. At zero hearts the explorer returns to the Practice Lodge with one emergency heart, retaining earned XP and badges.

Changing modes using **Change adventure** keeps unfinished sessions *separately by game mode and player profile*. Starting an entirely new game within a mode replaces that mode's active session. The existing legacy save key `naches_math_maze_v1` is retained.

## Wildlands gameplay

1. Choose Wildlands from the opening popup, your grade (1–12), a starter explorer, its color, and an answer mode (multiple choice or typed). You may change a character's appearance later from the left settings panel.
2. Explore a region. Grass and other distinct terrain may trigger a question encounter. Paths remain traversable; walls are impassable.
3. A Mathling has two shields; solve two questions to defeat it and earn XP. Wrong answers cost hearts and record the affected math skill **and answer number range**.
4. Use **Return to Practice Lodge**, or walk back to its house tile. Each correctly answered targeted practice question restores one heart. Missed practice provides a hint and a new question, with no additional heart loss. You may leave the lodge at any time.
5. Travel to the boss gate at the far side of the map. Correctly answer at least six of eight questions to earn the regional badge. For a lower-pressure option, timing is disabled by default. Optional timed boss mode gives three minutes for a regional badge, four for the Grand Summit.
6. Earn badges from all five regions to unlock the **Grand Summit** challenge: at least eight correct answers out of ten. Badges, XP, character selections, and final victories remain saved on your profile.

### The five regions

| Region | Math emphasis | Unlock |
|---|---|---|
| Orchard Fields | Addition and subtraction | Start |
| Whispering Forest | Multiplication and division | Orchard badge |
| Crystal Caverns | Fractions, decimals, and integers | Forest badge |
| River Crossing | Measurement, geometry, and percentages | Cavern badge |
| Summit Ruins | Algebra, powers, and mixed reasoning | River badge |

Problems adapt to the chosen grade. If a region's advanced math subjects are not appropriate for the selected grade, the encounter draws from supported introductory arithmetic skills instead.

### Explorer customization

- **Four starter appearances:** Scout, Ranger, Inventor, and Stargazer.
- **Four color palettes:** Teal, Rust, Violet, and Gold.
- **Four outfit sets:** Starter Gear (default), Orchard Explorer (35 XP), Forest Ranger (105 XP), and Cave Adventurer (205 XP).
- **Three visible equipment stages:** starter, upgraded gear at 90 XP, and advanced gear at 240 XP.
- Cosmetic options are earned through mathematical progress. They provide no competitive advantage.

Wildlands characters and maps are lightweight original SVG artwork embedded in `index.html`; encounter monster icons are simple thematic artwork rather than a collectible creature system. More sprite animation and additional outfits are potential future updates.

## Game controls

| Action | Control |
|---|---|
| Classic answer | Click corridor marker, use large answer button, or number keys 1–4 |
| Trailblazer direction | Click adjacent arrow or direction button |
| Wildlands movement | Arrow keys, WASD, touch D-pad, or click an adjacent tile |
| Wildlands answers | Click one of four choices or type a number/fraction, depending on setup |
| Practice / healing | Walk onto lodge tile or use Return to Practice Lodge |
| Change modes | Change adventure in page header |
| View hint | Show hint |

## GitHub Pages installation

Upload the **two files** in the GitHub ZIP to the root of the existing `math-maze-adventures` GitHub repository:

```
math-maze-adventures/
  index.html
  README.md
```

Then in the repository choose **Settings → Pages → Deploy from a branch → main → /(root)**. Use the existing Pages address and existing Naches Learning Hub card. **Do not create a separate repository or replace the Learning Hub `index.html`.**

Because `index.html` is self-contained, there are no additional CSS, JavaScript, or image files to upload.

## Saving and privacy

Progress is stored using browser `localStorage` under the existing key `naches_math_maze_v1`. It is **device/browser/profile-specific**. It does not sync across Chromebooks and is lost if the student clears site data or uses an ephemeral/guest Chrome profile. Avoid clearing site storage during an unfinished game. Saved older Classic and Trailblazer sessions remain compatible. A completed badge and cosmetic unlock remain available in that nickname profile.

## Testing and current limitations

Automated Chromium tests verified the initial three-mode popup, Classic exit visibility, Trailblazer question reveal, mobile viewport sizing, region path connectivity, question encounters, healing, all five boss badges, final boss completion, typed answers, cosmetic unlocking, separate mode-session restoration, and JSON serialization of an active Wildlands encounter. See `QA_RESULT.json` in the full package.

**This is a playable development preview.** Physical Chromebook/touchscreen testing and actual GitHub Pages persistence after closing/reopening the browser have **not** been verified. Question pacing, level balance, and the RPG artwork may need adjustments based on student playtests.

## License / project context

An original educational game inspired by familiar exploration-RPG mechanics. It does not use Pokémon characters, designs, or music. This project has not been assigned an open-source license; do not assume third-party reuse rights.
