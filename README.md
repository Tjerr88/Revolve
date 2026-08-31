# Revolve PWA

An installable, offline-ready version of Revolve for GitHub Pages.

## Publish with GitHub Pages

1. Create a new GitHub repository, for example `revolve`.
2. Upload **the contents of this folder** to the repository root.
3. Open **Settings → Pages** in GitHub.
4. Under **Build and deployment**, choose **Deploy from a branch**.
5. Select branch **main** and folder **/(root)**, then click **Save**.
6. GitHub will provide the public HTTPS address for the app.

## Install

- Open the GitHub Pages address in Chrome, Edge, or Safari.
- Use the always-visible **Install app** button in Revolve.
- If direct browser installation is unavailable, the same button shows device-specific instructions.
- On iPhone and iPad, installation is managed through **Share → Add to Home Screen**.

A service worker requires HTTPS or localhost. It cannot run when `index.html` is opened directly as a local file.

## Data

Sessions, loads, reps, rotations, active timers, and settings are stored locally in the browser. Nothing is sent to GitHub. Use **Settings → Back up & restore** to download or restore a validated JSON backup. Before an import replaces local data, Revolve automatically downloads a safety backup.

## Training record

- Every in-progress session is saved automatically and can be resumed after closing the app.
- History can be searched and filtered, with a separate overview per exercise.
- The most recent completed session can be removed and safely restored to its pre-completion state. Older entries can be corrected without changing the fixed program queue.
- Filled repetitions automatically determine the next load: two or three sets below the minimum reduce the load and all three sets at the maximum increase it. A larger `++` increase requires 7 / 7 / 10 for Strength, 11 / 11 / 15 for Hypertrophy, or 15 / 15 / 20 for Endurance. The current load field shows the direction by colour before the session is completed.
- Core and Accessory loads are stored per exercise, included in session history, and visible in the exercise overview without requiring repetition entry.
- Completed 18-session blocks include a compact progress summary.
- History includes a dedicated Blocks view. Because the three-phase exercise cycle repeats, Block 4 compares with Block 1, Block 5 with Block 2, and so on, using the best matching exercise loads in each block.

## Explosive work and daily readiness

Each three-block phase contains a fixed explosive exercise for Resistance A, B, and C. With a recovery total of at least 12 and no individual score below 3, Revolve places three explosive sets before the normal Strength work. On lower-readiness Resistance days the explosive block is removed.

Core and Accessory work is always planned and rotates after every completed Resistance session, independently of A/B/C and block completion. High-readiness days prescribe 2–3 included sets. Lower-readiness days make 1–2 sets optional; the pair still advances after the session even when skipped.

Every Core and Accessory exercise has its own repetition, time, or per-side prescription. Suitcase Carry uses 45–60 seconds per side and progresses in load only after every set reaches 60 seconds with level shoulders. Explosive work follows a quality stop rule: end the set as soon as speed, jump height, distance, or technique clearly drops.

The Lateral trunk category alternates Suitcase Carry with Side Bend. Side Bend uses 8–15 controlled repetitions per side without trunk rotation.

## Block transitions and deload

Returning exercises in a new phase start 10% below their last logged working load, rounded to 2.5 kg with at least a 2.5 kg reduction. From Block 2 onward, the first A, B, and C session are deload sessions: main and explosive work use two sets, the third fields are locked, Core and Accessory use 1–2 sets, and that session cannot change the next working load.

After the deload occurrence, the next normal occurrence of an exercise resumes automatic progression. The deload load, completed sets, and full session remain available in History.

## Optional Conditioning and timer signal

Conditioning is enabled by default. It can be disabled under **Settings → Conditioning activities** for people who manage their Zone 2 and interval work elsewhere. With it disabled, Resistance A, B, and C continue rotating directly and existing conditioning history remains intact.

The Android timer uses a louder native alarm-stream signal plus vibration so rest and interval transitions remain noticeable while music is playing. The web version uses a louder multi-tone fallback and vibration when the browser supports it. A test button is available in Settings.

The Android widget prioritizes the next session on its second line and uses a shorter status such as `DONE TODAY · 10:08` above it. Text scales on narrow widgets, and the widget can be resized horizontally.

## Kettlebell HIFT

Settings contains an intentionally hidden Kettlebell HIFT option. It can only replace the interval session currently next in the Conditioning queue; it can never replace Resistance, Zone 2, Recovery Guard, or Full Rest. It requires high readiness, fourteen days of build-up or cooldown, and creates one fixed no-reroll workout targeting 400 SU with a valid 360–440 SU range. Completing it consumes that exact interval position and advances the normal queue once.

Every generated HIFT covers squat, hinge, push, pull, core, and hybrid patterns, uses at most two blocks per pattern, and avoids duplicate exercises. The regular vertical hypertrophy press is Dumbbell Shoulder Press; Kettlebell Military Press remains in the HIFT exercise pool.

## Files

- `index.html` — the complete Revolve app
- `manifest.webmanifest` — installation settings and app icons
- `service-worker.js` — offline cache
- `background-revolve.webp`, `header-revolve.webp`, and `logo-revolve.webp` — brand imagery
- `icon-*.png` — app icons

All files are intentionally placed in this single flat directory. Upload them together to the repository root.
