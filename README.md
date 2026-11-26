# CS453 - After-Hours Cleaning Robot (Variant 3)

- **Student Name:** مؤيد اتيم الجعيدي
- **Student ID:** 09231196
- **Project:** After-Hours Cleaning Robot
- **Generated Variant:** Variant 3 (`start = 'S'`, `goal = 'D'`, `removed_edge = ('E', 'G')`)
- **Notebook:** `project.ipynb`

## Overview

This repository contains my individual two-week CS453 workbook implementation and explanations for the **After-Hours Cleaning Robot** problem on **Variant 3** (8 rooms, starting at `'S'`, cleaning target room `'D'`, with edge `('E', 'G')` removed).

## Files in This Repository

- `project.ipynb`: Complete notebook containing PEAS & environment analysis, state/action/transition/goal/cost representation, the cleaning simulator, BFS and A* implementations, heuristic admissibility discussion, sources/assistance disclosure, and the submission checklist.
- `README.md`: Project summary, variant details, file guide, dependencies, and execution instructions.

## Dependencies

- Python 3.10+ (tested in Google Colab with Python 3.13.18)
- Standard library modules only (`copy`, `platform`, `collections.deque`, `heapq`) — no external packages or GPU required.

## How to Run

1. Open `project.ipynb` in Google Colab (via GitHub or by uploading the notebook).
2. Ensure `STUDENT_ID = "09231196"` is set in the variant cell to generate Variant 3 (`start='S'`, `goal='D'`, `removed_edge=('E', 'G')`).
3. Run **Runtime > Restart and run all** and verify that the simulator, BFS, and A* reach `('D', True)` in `2` moves and pass all edge-case checks cleanly.

## Open in Colab

https://colab.research.google.com/github/maoyed/Maoyed-Al-Jaidi_Artificial-Intelligence-Project/blob/master/project.ipynb
