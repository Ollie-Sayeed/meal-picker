# Meal picker – to-do list

Things to work through when there's time. Newest ideas go at the bottom of "To do";
move items to "Done" (with the date) once finished.

## To do

From the 2026-11-08 review:

**List data (rows that can never be suggested)**
- [ ] Rows with a value missing, so the columns have shifted: `Ciabatta loaf` (no price), `Pea shoots` (no calories),
  `Choco malties` (cereal, no calories), `Maple and nut crisp` (cereal, one value missing – probably price).
- [ ] Rows skipped for lack of nutrition (placeholders?): `Sainsbury's banh mi ingredients` and four Waitrose houmous
  rows (Moroccan style, caramelised onion, roasted beetroot and mint, lemon and coriander).
- [ ] `Yutaka tofu gyozas` has 27.72g salt – probably a value from another column.

**Code**
- [ ] Decimal calories are misread (the decimal point is dropped, so 950.4 → 9504).
- [ ] Unticking "Toast" (allow as main meal item) doesn't remove toast from the search, unlike Crumpets/Muffins.
- [ ] Breakfast "Toast with Lotus Biscoff" is £0.24 vs £0.32 for the item version.
- [ ] Sauce-detection regex typo (`/\sauce\b/`); currently only misses the Wetherspoon curry-sauce dishes (no effect).
- [ ] Gym Kitchen meals are tagged but the tag is unused – should they count as non-solid like Leon/Flourish?
- [ ] Results title always says "multi-shop", even for a single shop.

**Food groups**
- [ ] Rice cereals (Rice Krispies, rice snaps, rice pops) and rice noodles count as rice, so need a curry/burrito.
- [ ] "Potato" group includes sweet potato soups/burgers, potato farls and "Tortilla chips…" (one potato per combo).
- [ ] Should "Vegetable tikka masala with pilau rice" stand alone like the no-chicken one?

## Done

- [x] 2026-11-07 – Put the tool on GitHub as `index.html` (from v49, restaurant priority).
- [x] 2026-11-07 – Sync saved lists across devices via `lists.json` in the repo.
- [x] 2026-11-08 – Restaurant food box is remembered and synced across devices for the rest of the day, and clears at midnight.
- [x] 2026-11-08 – Default breakfast is now the M&S maple syrup porridge.
- [x] 2026-11-08 – Salad: "Lambs lettuce" now counts as salad; "Four bean salad" no longer does (one shared rule).
- [x] 2026-11-08 – No shops ticked = no shopping: only pre-purchased items, fast food and restaurant food
  (plus always-at-home items – olive spread, burger relish, olive oil, Lotus Biscoff – and toast/crumpets/muffins
  if allowed; no avocado add-ons).
- [x] 2026-11-08 – Plain Lotus Biscoff is always available (treated as permanently pre-purchased).
- [x] 2026-11-08 – Sort options unbundled: "Prioritise restaurant food" and "Prioritise pre-purchased items" tickboxes
  (ranked first), then Item count or Price; results always displayed in price order. Allowed toast/crumpets/muffins
  stay £0 and count as pre-purchased.
- [x] 2026-11-08 – Sort choices (dropdown + prioritise tickboxes) are remembered and synced.
- [x] 2026-11-08 – Mobile layout: fits the screen, one column with the controls before the CSV list boxes,
  16px fields (no iPhone zoom), CSV rows don't wrap.
- [x] 2026-11-08 – Review fixes: breakfast English muffin 388 kcal; standalone rice meals (katsu curry with rice,
  no chicken tikka masala with pilau rice, Bol teriyaki rice bowl, Suhana cuppa fried rice); Masala fries not curry,
  Patak's potato and cauliflower curry is; Chips and curry sauce stands alone; tofu gyozas/Squeaky Bean slices not tofu;
  nut cereals not nuts; savoury chilli biscuits not chilli; burotis not naan/bread; Itsu soup dumplings not soup.
