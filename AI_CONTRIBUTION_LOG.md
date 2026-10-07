# AI Contribution Log – SLE-3 (Full C4 Model)

**Course:** 02AML204 – Introduction to Artificial Intelligence
**PRN:** 25UAM072  |  **Name:** Siddharth
**Date:** 04 October 2026
**AI tool used:** Claude (Anthropic), via the Claude chat app

## 1. What I asked the AI to do

| # | My request | What the AI produced |
| --- | --- | --- |
| 1 | Gave the SLE-3 guideline (.docx) and my SLE-1 and SLE-2 repository links, and asked it to prepare SLE-3 as the guideline says | Read the guideline and both repos, chose my SLE-2 Maze Solver (BFS/DFS) as the system, drew the Level 1–3 diagrams with a Python (matplotlib) script, and wrote the Word report in the required 8-section structure |
| 2 | Asked for a README and an AI contribution log for GitHub | This README.md and this log, plus the repo folder layout |

## 2. What the AI helped with

- Reading the guideline and following its exact structure and page limit (3 pages).
- Choosing the Maze Solver from SLE-2 as the system, as the guideline recommends.
- Drafting the diagrams: Context (Level 1), Container (Level 2, 6 boxes), Component (Level 3, Search Engine only).
- Writing the first version of the explanations, Level 4 code overview, design decisions and conclusion.
- Writing the helper scripts that draw the diagrams.

## 3. What I did myself

_(Edit this section so it is true for you. Only keep lines that you really did.)_

- Chose to continue with my own SLE-2 Maze Solver and provided the guideline and both repositories.
- Wrote and tested the original code in SLE-1 and SLE-2 (`maze_search.py` with `bfs()`, `dfs()`, `FlameProfiler` and so on).
- Checked every box in the diagrams against a real function or variable in my `maze_search.py`.
- Filled in my PRN, name, division and date, and renamed the file for Moodle upload.

## 4. What I verified

- [ ] Each container maps to real code (for example Search Engine → `bfs()` / `dfs()`; Visited Memory → `came_from`).
- [ ] The Level 3 loop matches the real `bfs()` / `dfs()` loop: pop → count → goal test → expand → skip seen → push.
- [ ] Level 4 lists only names that exist in `maze_search.py`. There is no `Node` class, because cells are `(row, col)` tuples.
- [ ] The report is 3 pages, within the 2–4 page limit.
- [ ] I can explain every diagram and design choice in my own words.

## 5. What I changed or would change

_(Fill in after you review. Example: "I reworded the conclusion in my own words" or "I corrected the name on the first page.")_

## 6. Honest summary

The diagrams, text and repo files were drafted by AI from my guideline and my existing code.
The system, the code and the final checking and submission are mine. I understand the design
and can explain it.
