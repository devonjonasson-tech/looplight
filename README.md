# Looplight: The Last Observatory
A mobile-friendly escape-room prototype. Explore three illustrated views, collect and use objects, decode related clues, restore an astronomical instrument, and unlock the exit. Includes a field journal, progressive optional hints, automatic local saves, and a restart confirmation. There are no timers or penalties.

The opening chapter contains five linked puzzle milestones and a complete ending. It is a single-room prototype, not a finished paid game. Original ten-level light puzzles remain available at `original/`.

## Run locally
Serve this directory with `python3 -m http.server 8080`, then open http://localhost:8080. No build is needed to play. All illustrations are local SVG; optional Google fonts fall back to system fonts. Progress is stored only in the browser; no analytics, payments, or accounts are implemented.

## Verify
Install development dependencies with `npm install`, install Chromium with `npx playwright install chromium`, start the local server, and run `npm test`. `GAME_URL` can target another deployment. The browser test exercises the complete escape path on a mobile viewport, incorrect-code rejection, inventory interactions, reload persistence, restart, overflow, and browser errors. Puzzle answers are intentionally present in the client source and test.

## Publish
The GitHub Actions workflow publishes the game and the original puzzles to GitHub Pages when main changes. Repository Settings → Pages must use GitHub Actions.

App Store delivery still requires native packaging, Apple Developer enrollment, signing, device testing, icons and screenshots, privacy disclosures, price configuration, and App Review. Title availability and trademarks have not been checked.
