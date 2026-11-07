# Haruku Fit

A workout app with a built-in interval timer. It's a single `index.html` file with no build step and no install. Open it in any browser on your phone or computer.

## What it does

- **Home:** a dashboard with a quick timer with its own work, rest, rounds-per-set, sets and set-break settings, your current workout, this week's stats and the routines you added. New users start with an empty dashboard and pick what goes on it from the Catalog.
- **My routines:** build, edit and save your own routines (name, work/rest times, repeats, and moves you tap or drag in, then drag to reorder), or copy a ready-made workout and change it. Star up to four to pin them on Home.
- **Share the app:** the share button in the top bar sends the app's link (by text message, WhatsApp or anything else). People who open it on a phone see short steps to put the app on their home screen.
- **Editing routines:** "Clear all moves" empties the list in one tap (with Undo) so you can refill it. The editor asks before throwing away unsaved changes. If you change a routine's moves or timing on the Timer, a bar offers to save those changes back to the routine.
- **Sharing routines:** tap Share on a routine to send a link. Opening the link adds the routine; you can also paste a link or code into the Catalog (handy for the home-screen app on iPhone, which doesn't share storage with Safari).
- **Music:** pick Deezer, Spotify, Apple Music or YouTube Music (and optionally paste a playlist link). Music never starts by itself: tap the music button on the timer and the app asks before opening it. If a workout is running it pauses and carries on when you come back. Beeps and the recorded Haruku coach voice work with or without music and mix over it instead of pausing it (iOS 16.4+, Silent mode off). If iOS cuts them off when the music app starts or stops, the timer shows a button to bring them back with one tap. The coach clips in `voice/` were made with the open Kokoro TTS model.
- **History:** every workout you finish (or stop after at least a minute of work) is saved on the device with the time you actually spent, so skipped intervals don't count, with weekly totals and a day streak. **Backup** copies everything (history, routines, settings) as a code or file you can restore after reinstalling or on another device.
- **Exercises:** 40 moves in four groups (Calisthenics, Strength, Stretch, Yoga). Each one has an animated figure that shows the movement, in a hand-drawn doodle style (the default, inspired by CocoMaterial's people illustrations), or a cartoon, realistic or stick-figure style, plus steps and a tip.
- **Ready-made routines (Catalog):** Upper Body, Core, Legs and Full Body sessions, plus a Morning Routine of stretches (40s holds, both sides) and a Leo Flow (bear side steps, squat to handstand, leg curl switch, breakdancer stretch, V-up toe touch). Tap Add to Home to put one on your dashboard.
- **Timer:** opens full screen with no top bar, so it is just the timer (the tabs at the bottom still take you elsewhere).
  - Use **Timer only** for your own workouts, or **With exercises** to follow the moves.
  - Set your own work, rest, rounds, sets and set break, or keep every round a fixed length (for example 45/15 = 1 minute).
  - Each set can have its own timing.
  - Beeps, an optional spoken coach, vibration, and the screen stays on while the timer runs.
- **Design:** Material 3 in a lighter blue and fresh green with white and red accents, with Eczar for titles and Plus Jakarta Sans for text. Icons are inline SVGs from Lucide (ISC license). Light mode and a warm charcoal dark mode.
- **Home screen help:** phone visitors see a banner on Home with a "Show me how" button that walks them through adding the app to the home screen (iPhone, Android, Samsung Internet, and in-app browsers like Instagram). Android Chrome also gets a one-tap Install button. The steps stay available under History.
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


## Checking the figures

`node tools/check-figures.js` measures every exercise animation (120 moments per loop, realistic style) and lists findings. It needs Playwright with Chromium.

- **Floor:** no part of the body drawn below the floor, and the figure never floats above it (jumps are expected to).
- **Bones:** no bone longer than in the standing pose. Shorter is fine, because a limb can point toward the viewer.
- **Knees:** in side views, knees never bend backwards.
- **Sliding:** hands, knees and feet resting on the floor stay in place.
- **Balance:** when only the feet carry the weight, the centre of mass stays over them.

Add `--sheet sheet.png` to also save a picture of every key pose, and look at it: the checks don't replace your eyes. Pass exercise ids (`node tools/check-figures.js squat,lunge`) to check a few. A deliberate exception goes in `ALLOW` at the top of the script, with the reason.

New front-facing exercises go in `FRONT` in `index.html`, so the realistic style places shoulders and hips correctly.
