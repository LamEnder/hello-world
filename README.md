# Loop Station

An Android app that plays music the way games do: the intro plays once, then the track loops
seamlessly between a loop start (A) and loop end (B) that you set yourself.

- Drag A and B on the waveform, nudge by milliseconds, or type exact seconds or samples
- Seam view and match score, plus auto-match to find the cleanest loop end
- Reads `LOOPSTART` / `LOOPLENGTH` tags (the RPG Maker format) and copies them for your files
- Visualizer with your own background image, for a full-screen "music video"
- Loop points are saved per file on the phone

## Install

Download `LoopStation.apk` from the `loop-station-apk` branch on your phone and open it.
Android will ask you to allow installs from your browser the first time.

## Build

Every push to the `loop-station` branch builds the APK with GitHub Actions and publishes it as a release.
Locally: `npm ci && npx cap sync android && cd android && ./gradlew assembleDebug`.

The app is the web page in `www/`, wrapped with Capacitor.
