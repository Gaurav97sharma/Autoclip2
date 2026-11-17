# Autoclip standalone (no server, no Termux)

Everything runs inside the browser on your phone. Projects, source videos and exported
clips are kept in IndexedDB on the phone until you delete them (My clips tab).

Files: index.html, style.css, app.js, sw.js (offline), manifest.webmanifest, icons/

## Install it like an app (recommended)
Chrome needs the files on an https address to install them as an app. Free options you can
do from a phone browser: GitHub Pages, Cloudflare Pages or Netlify.
1. Put all these files in one folder on the host, keeping the same file names.
2. Open the https address in Chrome on your phone.
3. Chrome menu (three dots) > "Install app" or "Add to Home screen".
Autoclip then opens full screen from your home screen and works offline.

## Make an APK file (optional)
Upload nothing to the Play Store. After the app is on an https address, a free web tool such as
pwabuilder.com can package it as an Android APK. Notes:
- An APK made this way may run in a plain WebView, which often does not support the microphone
  speech recognition used by "Auto-generate captions". Typing captions and importing .srt still work.
- The Chrome-installed app above has every feature, so use that if you can.

## What is different from the server version
- No link import (YouTube, Instagram and similar need a server). Choose a video file from the phone.
- Long or large videos (over about 1 hour or 250 MB) are scanned by playing them silently at 4x speed,
  so a 1 hour video takes about 15 minutes. A Skip button uses evenly spaced clips instead.
- Exports record the clip in real time in the browser at 1080p, so keep the app open while it exports.
- Keep Chrome open in the foreground during analysis and export.
