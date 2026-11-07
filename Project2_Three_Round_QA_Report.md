# Project 2 — Three-round improvement and QA report

This log documents the three improvement rounds required by page 5 of the BSERC Week 1 PDF.

## Round 1 — Requirements and structure audit
- Checked all three pages are standalone HTML documents with inline CSS and JavaScript.
- Checked each page includes a mobile viewport declaration and responsive media query.
- Checked no external JavaScript libraries or remote script URLs are required.
- Checked each page has at least five user-facing interactions.
- Checked the three selected project types are distinct: revision dashboard, money explorer, and decision helper.

## Round 2 — Functional and safety improvements
- DSA Sprint Dashboard: improved quiz completion behavior so the final score remains visible at the end instead of silently wrapping to a new round. Restart is explicit.
- Student Money Lab: escaped user-entered merchant/date/category text before rendering it into HTML, preventing typed text from being interpreted as markup.
- DSA Path Finder: retained validation for comparing two different options and retained reset behavior for priorities and notes.
- All transaction examples remain fictional and the duplicate checker clearly says matches require manual confirmation.

## Round 3 — Validation and edge-case review
- Ran Node.js syntax validation against the inline JavaScript in each HTML file. Results are recorded below.
- Audited document structure, viewport metadata, inline CSS/JS, lack of external script dependencies, and mobile media queries.
- Reviewed invalid/empty input handling: money transaction requires merchant, positive amount and date; path comparison warns if the same route is selected; empty decision notes are not saved.
- Reviewed timer controls (start/pause/reset), quiz restart, checklist reset, filter reset, transaction restore, and path finder reset.

## Automated checks
- **01_DSA_Sprint_Dashboard.html — PASS:** Inline JavaScript syntax valid
- **02_Student_Money_Lab.html — PASS:** Inline JavaScript syntax valid
- **03_DSA_Path_Finder.html — PASS:** Inline JavaScript syntax valid
- **01_DSA_Sprint_Dashboard.html — PASS:** single HTML document: yes; viewport meta: yes; inline CSS: yes; inline JavaScript: yes; no external script dependency: yes; mobile media query: yes
- **02_Student_Money_Lab.html — PASS:** single HTML document: yes; viewport meta: yes; inline CSS: yes; inline JavaScript: yes; no external script dependency: yes; mobile media query: yes
- **03_DSA_Path_Finder.html — PASS:** single HTML document: yes; viewport meta: yes; inline CSS: yes; inline JavaScript: yes; no external script dependency: yes; mobile media query: yes

## Manual test checklist (open each file in a browser before submission)
- [ ] Page 1: tick/un-tick checklist; reset; start, pause and reset timer; change duration; reveal/hide cards; next/previous; answer quiz; complete quiz; restart; filter complexity.
- [ ] Page 2: change category; search merchant; reset filters; move savings slider; change income; run duplicate check; add transaction; delete transaction; restore sample data.
- [ ] Page 3: change all three priority sliders; change time; recalculate; reset; compare two distinct options; select same option twice and confirm validation; generate each session length; save and clear note.
- [ ] Narrow screen: open each page in a phone-sized browser viewport and confirm cards stack and controls remain usable.

**Testing limitation:** The environment used for this build did not have a runnable browser binary, so a real click-through in Chrome/Safari on laptop and phone has not been performed here. Syntax and structural checks are automated; complete the manual checklist on your devices before submitting.