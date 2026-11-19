# Penny

Spend a little less each month. Penny records what you spend in a few taps, sets a target a bit lower than last month, and shows every day whether you are on track.

Live at https://yeochoi.github.io/penny/. Open it in Safari and choose Add to Home Screen.

- Everything stays on the phone in local storage. Settings has backup and restore.
- `design-system/` is the one source for colours, type and rules. Edit `tokens.json` or `README.md` there, then run `node scripts/build-design-system.mjs` to rebuild `tokens.css` and the design system page.
