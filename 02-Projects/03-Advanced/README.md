# ⚡ ADVANCED PROJECTS (Phase 2-4)

> These are portfolio-grade projects. Each one proves a different professional skill.
> Rules: real planning doc before code, git branch per project, tests for backend work,
> deployment required, README written for a stranger.

---

## Project #10 — Notes API (Client: "Second Brain Inc.")

**Stack:** Node.js + Express + SQLite · **Proves:** backend fundamentals

**Requirements:**
- REST endpoints: `GET /api/notes`, `GET /api/notes/:id`, `POST`, `PUT`, `DELETE`
- Proper status codes: 200, 201, 204, 400, 404 (not everything is 200!)
- Input validation on POST/PUT (reject empty titles, over-long bodies)
- Database persists across server restarts
- `.env` for config — never commit secrets (Mission 1 skill!)

**DoD:**
- [ ] Tested every endpoint with Postman or curl; status codes correct
- [ ] SQL injection test: try `'; DROP TABLE notes; --` as a title — must be harmless
- [ ] Server returns JSON errors: `{ "error": "Note not found" }`
- [ ] Deployed (Render/Fly.io) with a public base URL in the README
- [ ] At least 3 unit tests passing

---

## Project #11 — Real-Time Chat (Client: "TeamChat")

**Stack:** Node + Express + WebSockets (Socket.IO) · **Proves:** async architecture

**Requirements:**
- Multiple browser windows chat live with each other
- Username + message, message history buffer (last 50)
- "User joined / left" system messages
- Typing indicator ("Anna is typing...")

**DoD:**
- [ ] Open 3 tabs: all see messages instantly
- [ ] Server handles a client disconnecting mid-message without crashing
- [ ] Basic rate limiting: >5 messages/second gets ignored (think: why do companies need this?)

---

## Project #12 — Python Automation Suite (Client: "MySaneSelf")

**Stack:** Python · **Proves:** Python + real-world problem solving

**Three scripts in one repo:**
1. **File Organizer** — scans a folder, sorts files into subfolders by extension, dry-run mode by default
2. **News Scraper** — fetches headlines from a news site (respect `robots.txt`!), saves to CSV
3. **Password Generator** — CLI tool: length, symbols yes/no, strength estimate, saves to encrypted file

**DoD:**
- [ ] Each script has a `--help` flag (use `argparse`)
- [ ] No hardcoded paths — use `pathlib`
- [ ] Scraper handles "site unreachable" gracefully (try/except — no crashing)
- [ ] README shows exact run commands
- [ ] Virtual environment used (`python -m venv`) and documented

---

## Project #13 — Capstone: Full-Stack App of Your Choice

**Stack:** Your choice (React + Express, or Python/Django + templates) · **Proves:** you can build and ship

**Options (or propose your own):**
- E-commerce store: products, cart, checkout mock, admin panel
- Job-application tracker: apply → stages → notes, stats dashboard
- Study-buddy app: flashcards with spaced-repetition scheduling

**Requirements (all capstones):**
- User accounts (register/login, hashed passwords, JWT or sessions)
- Database schema you designed yourself — draw it first
- Responsive + accessible front-end (Phases 0-1 skills)
- Deployed publicly, live demo link
- Professional `README.md`: what it does, screenshots, how to run, tech used
- Written post-mortem: what you'd do differently — engineers grow here

**DoD:**
- [ ] A stranger can open the link and use it with zero explanation from you
- [ ] Your GitHub shows a clean commit history telling the project's story
- [ ] You can explain every line of your own code out loud

---

## 🧭 Post-Project Ritual (do this every time, like real teams)

1. **Self code review** — read your own diff: `git log -p` (yes, review yourself first)
2. **Lighthouse audit** — performance, accessibility, SEO scores
3. **Break it on purpose** — worst input you can think of
4. **Update the roadmap** — mark skills gained
5. **Write 3 bullet post-mortem** — what worked, what hurt, what to fix next time
