# Chess engine attribution and source

Stockfish is copyright its contributors, licensed under GNU GPL v3. The bundled engines are Stockfish.js, the WebAssembly/JavaScript port by Nathan Rugg and contributors.

The new, unmodified Stockfish 19 lite-single and full-single assets come from stockfish npm package **19.0.1**, release tag **v19.0.1**:

- Release and exact source: https://github.com/nmrugg/stockfish.js/releases/tag/v19.0.1
- Source archive: https://github.com/nmrugg/stockfish.js/archive/refs/tags/v19.0.1.zip
- GPL license bundled at `public/engines/stockfish19/LICENSE.txt`.
- Corresponding source is delivered alongside this app as `Stockfish-JS-19.0.1-source.zip`. Build instructions and network download configuration are in the archive's README.md and build.js.

The retained compatibility engine comes from stockfish npm package 16.0.0. Its WASM memory limits were previously patched for older Android devices; the application source includes the patch script `scripts/patch_wasm_test.js`. Source: https://github.com/nmrugg/stockfish.js/tree/v16.0.0 and license: https://github.com/nmrugg/stockfish.js/blob/v16.0.0/Copying.txt.

The old JavaScript fallback is used only if WASM initialization fails. The application must report the engine's actual UCI identity rather than advertise a neural network or modern version for this fallback.

Full neural Stockfish 19 requires roughly 95 MiB of bundled WASM assets. Lite uses a smaller neural network and is weaker than Full. Both single-thread variants avoid shared-memory requirements and can run offline after installation. On a WebView lacking WASM SIMD, selection falls back to Stockfish 16 automatically.

Before public distribution, preserve these licenses and make the complete corresponding engine source and modifications available to recipients. The current APK is a development build signed with the existing development certificate.

## Opening names and move sequences

Additional opening names, ECO codes and PGN move sequences are checked against https://github.com/lichess-org/chess-openings, released under CC0-1.0. Arabic teaching notes are original application text.
