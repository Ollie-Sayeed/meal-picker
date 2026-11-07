# meal-picker

A single-page meal planning tool: everything (HTML, CSS, JS) lives in `index.html`, served by GitHub Pages.

## lists.json is written by the live site
- The page syncs the user's saved lists (items, snacks, nuts, cereal, fast food, pre-purchased, frozen, etc.)
  to `lists.json` via the GitHub Contents API, committing to the repo's **default branch**
  (see the "CROSS-DEVICE SYNC" script at the bottom of `index.html`).
- So the remote branch gets new commits whenever the user edits lists in the browser:
  **always `git pull` before making changes, and pull again before pushing.**
- Multi-line lists are stored as arrays of lines under `form`. Keep it valid JSON if editing by hand;
  the field names match `collectPersistedState()` in `index.html`.
- If you add a new saved field, add it to `collectPersistedState()` / `applyPersistedState()` /
  `wirePersistence()`; it will sync automatically.
