# Haruku Fit

A workout app with a built-in interval timer. It's a single `index.html` file with no build step and no install. Open it in any browser on your phone or computer.

## What it does

- **Home:** a dashboard with a one-tap quick timer, your current workout, this week's stats and your favorite workouts.
- **My workouts:** pick moves in the Catalog, save them as your own workout, and star up to four to pin them on Home.
- **Log:** every workout you finish (or stop after at least a minute of work) is saved on the device, with weekly totals and a day streak.
- **Exercises:** 30 moves in four groups (Calisthenics, Strength, Stretch, Yoga). Each one has an animated figure that shows the movement, in a cartoon character or stick-figure style, plus steps and a tip.
- **Workouts:** ready-made Upper Body, Core, Legs and Full Body sessions.
- **Timer:**
  - Use **Timer only** for your own workouts, or **With exercises** to follow the moves.
  - Set your own work, rest, rounds, sets and set break, or keep every round a fixed length (for example 45/15 = 1 minute).
  - Each set can have its own timing.
  - Beeps, an optional spoken coach, vibration, and the screen stays on while the timer runs.
- **Design:** Material 3 in a lighter blue and fresh green with white and red accents, using the Plus Jakarta Sans font, light and dark mode.
- **Updates:** tap the sync button in the top bar to get the latest version. The app also checks when you open it.

Settings are saved in your browser.

## Run it

Live app: https://haruku08.github.io/workouts/

Or open `index.html` in any browser.

## Releasing an update

Bump the version in two places, then push to `main`:

1. `APP_VERSION` in `index.html`
2. `version.json`

Open apps then show "Version X is ready" with an **Update** button.
