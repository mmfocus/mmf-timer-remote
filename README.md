# MMF TIMER REMOTE — Separate GitHub Pages repository

This is a **new** version. Do not upload it to your existing `event-countdown-timer` repository.

## Deploy
1. On GitHub, create a **public** repository named `mmf-timer-remote`.
2. Extract this ZIP and upload **all files**, directly to the new repository root (not the ZIP or a subfolder). Commit.
3. Go to Settings > Pages > Build and deployment > Deploy from a branch. Select `main` and `/ (root)`, then Save.
4. Wait for deployment. Your new site will usually be `https://YOUR-USERNAME.github.io/mmf-timer-remote/`.
5. Open the new site on both devices. On the laptop select CONTROLLER and note the six-character room code. On the iPad select DISPLAY, enter that code, and tap CONNECT.
6. Keep both pages open, and keep the laptop awake. On the iPad, use Safari > Share > Add to Home Screen to install the separate remote app with the yellow MF icon.

## What it does
- Controller: start/pause, reset, presets, +/- time, time of day, speaker message SHOW/HIDE, colors and custom minutes.
- Display: fullscreen timer/message in the large display rectangle; follows controller state. Countdown continues underneath a speaker message.
- Supports multiple display devices using the same room code.
- THIS DEVICE mode works as a standalone timer if no connection is needed.

## Important limitations
- Both devices need working internet, even if on the same Wi-Fi. The app uses PeerJS's public demonstration signaling service and the PeerJS CDN. This is suitable for initial testing, **not guaranteed production uptime**. For paid live events, use a dedicated signaling service or a hosted real-time backend and test on-site.
- Room codes are convenience pairing, **not authentication**; avoid confidential speaker messages.
- If the network disconnects, the display continues its last received countdown estimate but cannot receive new controller actions until you reconnect. Reload or tap CONNECT to rejoin.
- Browser/iPad backgrounding can suspend web connections; keep both screens active.
- There is no service worker, to avoid serving stale versions.
