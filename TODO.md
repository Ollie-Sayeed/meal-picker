# Meal picker – to-do list

Things to work through when there's time. Newest ideas go at the bottom of "To do";
move items to "Done" (with the date) once finished.

## To do

- [ ] **Nice, user-friendly mobile layout.** Right now the page is wider than a phone screen, so you have
  to scroll sideways (the title, results table and CSV boxes overflow).
- [ ] **Restaurant food box lasts until midnight.** When populated, it should survive reloads and closing
  the page for the rest of the day, then clear itself at midnight. (Up to v49 it isn't saved at all.)
  Open question: sync it across devices too, or keep it on the device where it was entered?
- [ ] **Check the definition of "salad".** Minor – review how the code decides what counts as a salad.
- [ ] **Change the sort options.** Details to decide when we get to it.
- [ ] **Default breakfast → M&S porridge.**
- [ ] **No shops ticked = no shopping trip.** In "Shops to consider", when no shops are selected, only show
  combos that need no shop at all, i.e. made only from pre-purchased items, fast food and restaurant food
  (where there is any).

## Done

- [x] 2026-11-07 – Put the tool on GitHub as `index.html` (from v49, restaurant priority).
- [x] 2026-11-07 – Sync saved lists across devices via `lists.json` in the repo.
