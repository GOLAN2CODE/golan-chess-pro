# Golan Chess Pro

[العربية](README.ar.md)


Android chess, training and analysis in Arabic and English. Current version: **1.11.0 (16)**. Application ID: `com.ibngolan.chess.pro`.

## Download and install

Download the APK and complete source ZIP from [Releases](https://github.com/dark9guna/golan-chess-pro/releases). Extract the source ZIP before running the build commands below. Full and Lite are alternative packages of the same application: install one. Both supplied APKs are existing **Debug** builds; they were copied without rebuilding or changing their signatures. Android 7 / API 24 or later is required. Full includes the larger Stockfish 19 network; Lite saves space and has lower playing strength. Save an application backup before updating; replacing an existing installation requires a matching signing certificate.

```powershell
adb install -r Golan-Chess-Pro-1.11.0-Full.apk
# Or install Golan-Chess-Pro-1.11.0-Lite.apk
```

## Features

- Engine play, local play, direct peer challenges, engine matches and tournaments, clocks with Fischer increments, and match recovery.
- Stockfish 19 Full/Lite, Stockfish 16 compatibility, legal move validation, one premove, promotion, board arrows and square colors.
- PGN import/export, FEN position editor, local game archive, engine review with evaluation graph, practice retries and mistake notebook.
- 49 reference opening lines, 1,101 local puzzles, daily training, puzzle storm and local backup. Arabic/English, light/dark themes, piece styles, sound and device-supported voice input.

## Build from the source ZIP

Install Node.js compatible with the locked Vite/Capacitor toolchain, npm, JDK 21, Android SDK API 36 and the Gradle wrapper prerequisites. The package lock and Gradle files define the dependency versions. Network access is required to restore dependencies. Start in the extracted source root containing `package.json`.

```powershell
npm ci
npm run dev
# Android Full
$env:GOLAN_ENGINE_PACKAGE = 'full'
npm run build
npx cap sync android
Set-Location android
.\gradlew.bat assembleDebug
```

For Lite, repeat from the source root with `$env:GOLAN_ENGINE_PACKAGE = 'lite'` and use `.\gradlew.bat :app:clean :app:assembleDebug` after syncing. Configure your own SDK path locally. Signing keys and workstation configuration are intentionally absent. A locally rebuilt Debug APK may not update the supplied APK if its certificate differs. Release signing must use your own private configuration.

Existing checks can be run with `npm test`, `npm run lint` and `npm run test:ui`; browser checks need installed Chrome or `GOLAN_BROWSER`. These checks were preserved, but no app build or functional test was run for this publication package.

## Limitations and licenses

Engine strength and review accuracy are application estimates, not an official Elo calibration or another service's proprietary scoring. Online challenges, extra puzzle sources, voice input and tablebases depend on network or device services. No account server, global ranking, matchmaking or anti-cheat service is included. The opening catalog is instructional, not global game statistics. Offline engine performance depends on the device/WebView, with compatibility fallback when needed.

Preserve `THIRD_PARTY.md`, the bundled GPL text and both official corresponding-source archives in `Engine-Sources/`. The application also retains a legacy JavaScript fallback whose exact corresponding source revision is not established by those two archives. See `LICENSE_STATUS.md` for the unresolved distribution issue. No new license is assigned to the owner's application code. See `PRIVACY.md` for data handling notes.
