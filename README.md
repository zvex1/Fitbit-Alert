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

## Notes
- Your watch or tracker must broadcast the standard BLE heart rate profile. Many Fitbit/Google devices
  only do this in a specific mode (e.g. "Heart rate on equipment" / HR broadcast during an exercise).
- "Play through silent mode" (on by default) asks iOS for media-style sound so alerts play even when the
  phone is on silent. It takes effect on your next tap of Connect, Reconnect or Test.
- iOS pauses audio when Bluefy is in the background, so keep the page on screen.
