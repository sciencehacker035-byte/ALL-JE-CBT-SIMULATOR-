# CBT Simulator (Civil JE) – static site
Pure HTML/CSS/JS. Progress lives in browser LocalStorage. No backend.
## Deploy on GitHub Pages
Push this folder to a repo → Settings → Pages → Deploy from branch `main` / root. Paths are relative, so project sub-paths work.
## Add questions
Append objects to `data/questions.json` (or add new files and list them in `DATA_FILES` in `js/config.js`). IDs must be unique, `correctAnswer` is 0–3, difficulty is Easy/Medium/Hard, `section` is `Technical` or `Non-Technical`. Problems are logged in the browser console on load.
Label unverified items `PYQ-style / Practice Question`; only use `PYQ` with a verified exam, year and shift.
## Exam patterns
`js/config.js` values are **unverified placeholders**. Check the official notification and edit them.
## Wrong-question memory
Each question stores attempts/correct/wrong/streak/last. A mistake is *mastered* after `MASTERY_THRESHOLD` (3) consecutive correct answers in separate tests. New tests reserve up to 40% of slots for due mistakes, ranked by priority (wrong count, low streak, time since last attempt).
## Limits
JavaScript cannot provide real anti-cheating. Progress is per browser, so use Export/Import to move it.
