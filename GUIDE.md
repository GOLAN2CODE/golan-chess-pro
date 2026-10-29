# Golan Chess Pro — practical guide

[العربية](GUIDE.ar.md) · [Overview and source build](README.md) · [Downloads](https://github.com/GOLAN2CODE/golan-chess-pro/releases)

## Install and choose an engine package

Version 1.11.0, Android build 16, requires Android 7 / API 24 or later. Choose one APK: Full bundles the larger Stockfish 19 neural network; Lite is smaller and weaker. They share an application ID and are alternatives, not separate accounts. Both supplied APKs are development Debug builds. Back up existing app data before updating; Android requires a matching signing certificate to replace an installed copy.

## Play and study

For solo practice, start an engine game and choose the available engine, time control and playing options. Local play lets two people share one device. Clocks support Fischer increments. Engine matches and tournaments help compare the bundled engines; their strength labels are not officially calibrated Elo ratings. Direct peer challenges connect players using a room code and need working network connectivity; no matchmaking service, global rating or anti-cheat system is included.

Move by tapping or dragging, select a promotion piece when required, and enable a single premove if desired. A premove is checked again before execution. Board colors, piece designs, light/dark appearance and sound are adjustable. Voice moves depend on the device/browser speech service and microphone access; typed and touch controls remain the practical fallback.

Use puzzles to practice finding a move, daily training for a short routine, or puzzle storm for timed practice. The installed catalog contains 1,101 local puzzles. The opening explorer contains 49 reference lines that can be played through or used as starting positions. These are teaching material rather than a database of worldwide game frequencies.

## Bring in positions and keep results

PGN imports bring recorded games into the archive/review workflow; PGN export lets you share them with compatible chess tools. FEN describes one position and can be used with the position editor. Check the position before starting a new game. Engine review adds evaluation, an evaluation graph and variations; retry exercises and the mistake notebook turn reviewed positions into local practice. Accuracy/classification scores are this app's estimates, not another chess service's proprietary analysis.

Keep an application backup outside the phone when important progress should survive device loss. Backups and PGN exports are user-controlled files; sharing sends selected content to the Android destination you choose. Consult [data handling](PRIVACY.md) before using external services.

## Connectivity, cost and PC FAQ

Bundled engines, local games and installed training material run on the phone. Extra puzzles use public Lichess/Hugging Face endpoints, endgame lookups use a public tablebase service, and peer play/speech may need external services. Availability, rate limits and speech behavior can change. Device memory and WebView support affect engine selection and performance.

A focused source review found no personal billed API key, AI-credit consumption or payment integration. Network/mobile-data charges may still apply. **Your computer and Codex do not need to remain running after installation.** Building from source needs development tools; using the installed app does not. See [license status](LICENSE_STATUS.md) and [third-party information](THIRD_PARTY.md) for distribution details.
