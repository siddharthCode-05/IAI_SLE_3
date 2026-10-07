# IAI_SLE

# SLE-3: Architectural Design using the Full C4 Model

**Course:** 02AML204 – Introduction to Artificial Intelligence
**PRN:** 25UAM072  |  **Name:** Siddharth  |  **Division:** _A / B (fill in)_
**Builds on:**
- SLE-1 (Agent code): https://github.com/siddharthCode-05/IAI-SLE-25UAM072
- SLE-2 (Profiling BFS vs DFS): https://github.com/siddharthCode-05/IAI-SLE-2-profiling

> SLE-1 = Code. SLE-2 = Performance. **SLE-3 = Full Architecture Design.**

## What this project is

SLE-3 documents the architecture of my SLE-2 **Maze Solver System** (`maze_search.py`),
which solves a 10 × 12 grid maze with **BFS** and **DFS**, counts nodes expanded,
and measures run time. The architecture is drawn at all four levels of the C4 model:
**Context → Container → Component → Code**.

## Repository contents

| Path | Description |
| --- | --- |
| `SLE3_25UAM072_Siddharth.docx` | Final SLE-3 report (3 pages) submitted on Moodle |
| `diagrams/c4_level1_context.png` | Level 1 – Context diagram |
| `diagrams/c4_level2_container.png` | Level 2 – Container diagram (6 containers) |
| `diagrams/c4_level3_component.png` | Level 3 – Component diagram of the **Search Engine** |
| `scripts/draw_levels_1_2.py` | Python (matplotlib) script that draws the Level 1 and 2 diagrams |
| `scripts/draw_level_3.py` | Python (matplotlib) script that draws the Level 3 diagram |
| `AI_CONTRIBUTION_LOG.md` | Honest log of how AI was used in this SLE |

## The four C4 levels in brief

1. **Context** – User → Maze Solver System → path, nodes expanded, timing and images. Only external pieces: Python runtime and Matplotlib.
2. **Container** – Maze Input Module, Search Engine, Visited Memory, Timing & Profiling, Output Module, Results Store.
3. **Component** (inside Search Engine) – Frontier / Open List, Node Counter, Goal Test, Node Expander, Explored Check, Path Reconstructor.
4. **Code** – `neighbors()`, `bfs()`, `dfs()`, `_reconstruct_path()`, `FlameProfiler`, `time_algorithm()`, `print_maze_with_path()`, `render_maze_image()`.
   (Cells are plain `(row, col)` tuples, so there is no separate `Node` class.)

## Key design decisions

- BFS and DFS differ only in how the Frontier removes cells (front of a queue vs top of a stack).
- One `came_from` dictionary serves as both the visited set and the parent links for path rebuilding.
- Timing and profiling sit outside the search code, so measuring never changes results.
- A Heuristic Module could be added later for A* without changing the other containers.

## How to regenerate the diagrams

```bash
pip install matplotlib
python scripts/draw_levels_1_2.py   # writes Level 1 and Level 2 PNGs
python scripts/draw_level_3.py      # writes the final Level 3 PNG (run this one last)
```

Run the scripts from the folder where you want the PNG files written.
Run `draw_level_3.py` **after** `draw_levels_1_2.py`, because the first script also writes an older
draft of the Level 3 image, which the second one replaces.

## AI usage

AI (Claude) was used to help draft the diagrams and the first version of the explanations.
See [`AI_CONTRIBUTION_LOG.md`](AI_CONTRIBUTION_LOG.md) for the full, honest breakdown.

## What I learned

C4 explains one system at four zoom levels. Splitting the Maze Solver into containers and
components showed me which parts are search logic, which are data, and which are only measurement.
