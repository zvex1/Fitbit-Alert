# Fitbit Alert

A single-file web page (`index.html`) that connects to a heart rate sensor over Web Bluetooth
(standard Heart Rate service `0x180D`) and alerts you when your heart rate stays at or above a
target for 5 seconds, so you know you're done warming up.

Open it in **Bluefy** on iPhone (or Chrome on Android/desktop). It needs HTTPS, so serve it from GitHub Pages.

## Publish on GitHub Pages
1. Merge this branch into `main`.
2. In the repo, go to **Settings → Pages**.
3. Under **Build and deployment**, set Source to **Deploy from a branch**, Branch to **`main`**, folder **`/ (root)`**, then click Save.
4. After a minute or two the site is at `https://zvex1.github.io/Fitbit-Alert/`.

## Using it
1. Tap **Connect** and pick your tracker.
2. Pick **Warm-up** (alert when heart rate rises to the target) or **Cool-down** (alert when it drops to the target).
   Each mode remembers its own target. Set it, then tap **Arm** when you start.
3. When your heart rate holds at the target (at or above for warm-up, at or below for cool-down) for 5 seconds, the alert fires once and disarms itself.
   Tap **Arm** again for another round. Switching modes disarms the alert. **Test alert** previews the chosen alert without arming anything.

## Notes
- Your watch or tracker must broadcast the standard BLE heart rate profile. Many Fitbit/Google devices
  only do this in a specific mode (e.g. "Heart rate on equipment" / HR broadcast during an exercise).
- Alerts mix with music from other apps instead of pausing it. The iPhone silent switch mutes them,
  so keep the ringer on.
- iOS pauses audio when Bluefy is in the background, so keep the page on screen.
