# CS453 AI Project - After-Hours Cleaning Robot

**Student:** مؤيد اتيم الجعيدي (09231196)  
**GitHub username:** maoyed  
**Project choice:** Cleaning Robot  
**Assigned variant:** Variant 3 (`start = 'S'`, `goal = 'D'`, `removed_edge = ('E', 'G')`)

## Open the notebook

[Open in Colab](https://colab.research.google.com/github/maoyed/Maoyed-Al-Jaidi_Artificial-Intelligence-Project/blob/master/project.ipynb)

Public repository (`Maoyed-Al-Jaidi_Artificial-Intelligence-Project`, branch `master`).

## Task and scope

The robot moves between connected rooms in an 8-room graph (`'E'-'G'` removed) starting from `'S'` to clean room `'D'`, ending at `('D', True)` in the fewest moves. Hallways are clear, moves to neighbors succeed, and cleaning happens in one step at the goal.

## Files and environment

- `project.ipynb`: simulator, BFS, A*, outputs and explanations.
- `README.md`: project notes and run steps.

Uses Python 3 standard library (`copy`, `platform`, `collections.deque`, `heapq`) on Colab (Python 3.13.18).

## Run steps

1. Open `project.ipynb` in Colab from GitHub or upload it.
2. Check that `STUDENT_ID = "09231196"` generates Variant 3 (`start = 'S'`, `goal = 'D'`, `removed_edge = ('E', 'G')`).
3. Restart and run all cells, then check the output (`['S', 'A', 'D']`, `('D', True)`, `moves: 2`).

## Progress

| Milestone | Date | Commit link | Evidence |
|---|---|---|---|
| Setup | 2026-11-13 | https://github.com/maoyed/Maoyed-Al-Jaidi_Artificial-Intelligence-Project/commit/53ee4f8c12c7370c5bf66658380275d651ed0c0f | Name, ID and Variant 3 setup |
| Agent and simulator | 2026-11-22 | https://github.com/maoyed/Maoyed-Al-Jaidi_Artificial-Intelligence-Project/commit/329d1a3105c8c66912f5d24a9091e97e18a5aa9e | Simulator and checks |
| BFS baseline | 2026-11-21 | https://github.com/maoyed/Maoyed-Al-Jaidi_Artificial-Intelligence-Project/commit/9e3ee1218530d9c466ab40731617607087a02adc | BFS implementation and run |
| A* search | 2026-11-22 | https://github.com/maoyed/Maoyed-Al-Jaidi_Artificial-Intelligence-Project/commit/a5cbe445ec699c95f6b96a759ac01f24d5c94632 | A* implementation and run |

## Search methods

BFS checks nodes level by level with a FIFO queue without a heuristic, so it finds the fewest moves (`['S', 'A', 'D']`, `2` moves, `('D', True)`) on unit-cost graphs. A* uses `f(n) = g(n) + h(n)` with a priority queue and checks the goal when popping a node. Because removing `('E', 'G')` cannot make paths shorter, the supplied heuristic `h(n)` stays admissible on Variant 3 and also gives `['S', 'A', 'D']` (`2` moves, `('D', True)`).

## Sources and assistance

- CS453 workbook (`REFERENCE_GRAPH`, `VARIANTS`, `make_variant()`, `HEURISTICS`).
- Russell & Norvig, *Artificial Intelligence: A Modern Approach* (4th ed.), Chapter 3, and `aima-python` for reference on search ideas.
- Used AI help to draft and check parts of the text and code, and tested the notebook in Colab.
