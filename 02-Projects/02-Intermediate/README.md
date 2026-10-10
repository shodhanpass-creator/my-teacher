# 🚀 INTERMEDIATE PROJECTS (Phase 1)

> Rules of engagement (like real company work):
> 1. Read the FULL brief before writing code.
> 2. Plan first: sketch the UI on paper, list the files you'll create.
> 3. Start a NEW git branch for each project: `git checkout -b project/netflix-clone`
> 4. Commit in small steps with meaningful messages.
> 5. Definition of Done (DoD) must be 100% checked before a project counts.

---

## Project #6 — Netflix Landing Page (Client: "StreamFlix")

**Story:** A startup needs a marketing landing page that looks like a world-class product.

**Requirements:**
- Hero section with headline + CTA button
- 3+ rows of horizontal content ("Trending", "My List", "New Releases") using CSS Grid or Flexbox
- Fully responsive: 1 column on phone, proper grid on desktop (test with DevTools device mode)
- Hover effects on cards (scale/shadow), no layout jumping
- Dark theme, your own color palette (do NOT copy Netflix's exact branding — trademark!)

**DoD:**
- [ ] No horizontal scrollbar at 320px width
- [ ] All images have `alt` attributes
- [ ] Keyboard: Tab through the page, focus is always visible
- [ ] At least 8 meaningful commits
- [ ] Deployed (GitHub Pages or Netlify)

**Stretch:** Add a FAQ accordion using only `<details>/<summary>` + CSS.

---

## Project #7 — Memory Card Game (Client: "KidLearn Games")

**Story:** Educational client wants a pattern-memory game for children.

**Requirements:**
- Grid of cards (4x4), each card shows an emoji/symbol, all hidden at start
- Click two cards: match → stay revealed; no match → flip back after 1 second
- Move counter + timer + win screen
- Difficulty levels: Easy (3x3), Medium (4x4), Hard (6x6)

**DoD:**
- [ ] Game state stored in one clear object/array (not scattered variables)
- [ ] No bugs when clicking rapidly (guard against double-clicks — think: how?)
- [ ] Win screen shows time + moves
- [ ] Reset button starts a fresh game
- [ ] Deployed

**Stretch:** Save high scores to `localStorage` and show a scoreboard.

**Engineering hint (senior tip):** Model each card as `{ id, symbol, isFlipped, isMatched }`. Data first, rendering second. That single habit separates juniors from seniors.

---

## Project #8 — Expense Tracker (Client: "Budgetly FinTech")

**Story:** FinTech startup MVP. Users track daily spending.

**Requirements:**
- Add expense: description, amount, category (select), date
- **Real `<form>` with validation** (this uses Mission 4 skills): amount must be number > 0, description required and max 50 chars
- List of expenses, sorted by date, with delete button
- Monthly total per category
- Persist in `localStorage`

**DoD:**
- [ ] Uses `<form>`, `<label for>`, `<select>` — not divs pretending to be inputs
- [ ] Invalid input shows a visible, accessible error message (`aria-live`)
- [ ] XSS test: try entering `<img src=x onerror=alert(1)>` as description — it must display as TEXT, not run
- [ ] Deployed

**Stretch:** Export expenses as CSV (string building + `Blob` + download link).

---

## Project #9 — Accessible Contact Form (Client: "InclusiveCo")

**Story:** Company was sued for an inaccessible website. Your form must be perfect.

**Requirements:**
- Fields: name, email, subject (select), message (textarea), newsletter checkbox
- Full keyboard operation, logical tab order
- Screen-reader friendly: labels, `aria-describedby` for hints, error announced via `aria-live="polite"`
- Client-side validation + success message
- No backend needed — simulate submit with `setTimeout` + loading spinner

**DoD:**
- [ ] Unplug your mouse: complete the entire form using only keyboard
- [ ] Run Lighthouse accessibility audit → score 95+
- [ ] Every input has a programmatically associated `<label>`
- [ ] Deployed

**Stretch:** Add `prefers-reduced-motion` media query to disable the spinner animation for users who request it.

---

## 🧭 How to plan any project (steal this process)

1. **Requirements** → restate them in your own words
2. **Split HTML** → header / main / footer, sketch boxes
3. **Data model** → what does one "thing" look like? (todo, card, expense)
4. **State** → where does the data live? (array? localStorage?)
5. **Render function** → one function that draws the UI from the data
6. **Events** → what can the user do? Map each to a state change
7. **Test edge cases** → empty input, huge input, rapid clicking, refresh mid-session
