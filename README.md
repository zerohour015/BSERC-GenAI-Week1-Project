# BSERC GenAI Internship — Week 1 Projects

**Owner:** [zerohour015](https://github.com/zerohour015)  
**Repository:** [BSERC-GenAI-Week1-Project](https://github.com/zerohour015/BSERC-GenAI-Week1-Project)

This repository contains the prepared deliverables for both projects in the BSERC Week 1 brief.

## Project 1 — Source-grounded AI Notebook

Folder: [`Project1_NotebookLM/`](Project1_NotebookLM/)

Prepared materials:
- [NotebookLM setup guide](Project1_NotebookLM/Project1_NotebookLM_Setup.md) — notebook title, student track, source import plan, source-grounding instructions, test prompts and feature checklist.
- [Source register](Project1_NotebookLM/Project1_Source_Register_and_Setup.md) — seven recommended MIT OpenCourseWare sources across web pages, PDF lecture notes and YouTube lectures.
- [DSA study guide](Project1_NotebookLM/DSA_Study_Guide.md) — insertion sort, binary insertion sort, merge sort recurrence and BST operations, grounded to the listed lecture sources.
- [12-question quiz and answer key](Project1_NotebookLM/DSA_Quiz_and_Answer_Key.md).
- [16 flashcards](Project1_NotebookLM/DSA_Flashcards.csv).
- [Mermaid mind-map source](Project1_NotebookLM/DSA_Mind_Map.md).
- [Responsive infographic](Project1_NotebookLM/DSA_Infographic.html).
- [Eight-slide interactive browser deck](Project1_NotebookLM/DSA_Slide_Deck.html).
- Audio narration script and video storyboard.
- [Notebook verification log](Project1_NotebookLM/Project1_Verification_Log.md).

**Important distinction:** These are prepared companion assets and NotebookLM setup materials. The actual NotebookLM notebook has not been created in the owner's Google account from this repository. NotebookLM Studio outputs (Audio/Video Overview, Studio mind map, Studio quiz/flashcards/infographic/slide deck), citation clicks, and the public NotebookLM share link must still be generated and verified inside NotebookLM. Do not treat the prepared scripts, HTML files or quiz as proof that those NotebookLM features were used.

## Project 2 — Thinking in HTML

Folder: [`Project2_HTML_Pages/`](Project2_HTML_Pages/)

Three standalone, responsive HTML pages, with inline CSS and JavaScript:
1. [DSA Sprint Dashboard](Project2_HTML_Pages/01_DSA_Sprint_Dashboard.html) — topic checklist, progress, focus timer, flashcards, scored quiz and complexity filter.
2. [Student Money Lab](Project2_HTML_Pages/02_Student_Money_Lab.html) — fictional sample spending, category/search filters, savings slider, possible-duplicate review, and add/delete/restore controls.
3. [DSA Path Finder](Project2_HTML_Pages/03_DSA_Path_Finder.html) — priority sliders, live study-route rankings, comparison, plan generator and decision notes.

Also included:
- [Prompts file](Project2_Prompts.txt)
- [Three-round QA report](Project2_Three_Round_QA_Report.md)

All three pages are standalone and do not require external libraries, APIs, or a server. Student Money Lab uses fictional sample data only. Its duplicate checker flags matching merchant/amount/date combinations for human review; it does not access real banking data and a match is not proof of a duplicate.

## Test and submission notes

The QA report records static syntax/structure checks and the outstanding manual browser/phone interaction checklist. Run those manual checks before claiming full device testing.

The BSERC brief calls for two separate portal submissions at https://ai.bserc.org/projects:
- **Project 1:** paste the viewable NotebookLM share link in the Demo / Video / Presentation link field.
- **Project 2:** upload a ZIP containing the three final HTML files and `Project2_Prompts.txt` (under 10 MB).

The GitHub repository is a code/evidence location; it does not replace either required BSERC submission.
