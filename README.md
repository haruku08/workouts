# Haruku Fit

A workout app with a built-in interval timer. It's a single `index.html` file with no build step and no install. Open it in any browser on your phone or computer.

## What it does

- **Home:** a dashboard with a quick timer with its own work, rest, rounds-per-set, sets and set-break settings, your current workout, this week's stats and your favorite workouts.
- **My routines:** build, edit and save your own routines (name, work/rest times, repeats, and moves you tap or drag in, then drag to reorder), or copy a ready-made workout and change it. Star up to four to pin them on Home.
- **Music:** pick Deezer, Spotify, Apple Music or YouTube Music (and optionally paste a playlist link) to have the app open it when you press Start. Playback itself starts in the music app.
- **Log:** every workout you finish (or stop after at least a minute of work) is saved on the device, with weekly totals and a day streak.
- **Exercises:** 35 moves in four groups (Calisthenics, Strength, Stretch, Yoga). Each one has an animated figure that shows the movement, in a cartoon, realistic or stick-figure style, plus steps and a tip.
- **Workouts:** ready-made Upper Body, Core, Legs and Full Body sessions, plus a Morning Routine of stretches (40s holds, both sides).
- **Timer:**
  - Use **Timer only** for your own workouts, or **With exercises** to follow the moves.
  - Set your own work, rest, rounds, sets and set break, or keep every round a fixed length (for example 45/15 = 1 minute).
  - Each set can have its own timing.
  - Beeps, an optional spoken coach, vibration, and the screen stays on while the timer runs.
- **Design:** Material 3 in a lighter blue and fresh green with white and red accents, with Eczar for titles and Plus Jakarta Sans for text, light and dark mode.
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

