# 26S2 Exam Cheatsheets

Exam cheatsheets for Semester 2, 2026 (University of Sydney), in the 2-page A4-landscape LaTeX format used for the earlier COMP5270 sheet (`multicols` 3 columns, `\concept` / `\kh` / `\lbl` macros, pdflatex).

| Unit | Exam | Cheatsheet allowed | Files |
|---|---|---|---|
| INFO6007 Project Management in IT | 25 Nov 17:00, MacLaurin Hall | Yes: one A4 sheet, double-sided, handwritten or typed | [`INFO6007/`](INFO6007/) |
| ELEC5620 | 17 Nov | No (closed book) | — |
| CSYS5030 | 19 Nov | No (closed book; formula sheet supplied in paper) | — |
| COMP5416 | 20 Nov | No (closed book) | — |
| COMP5318 | 27 Nov | No (closed book; calculator only) | — |

## Build

```sh
cd INFO6007
pdflatex INFO6007_cheatsheet.tex   # must stay at exactly 2 pages
```

Page fonts are set by `\PONE` and `\PTWO` near the top of the `.tex`. After edits, check `pdfinfo INFO6007_cheatsheet.pdf` still reports `Pages: 2`.

## INFO6007 contents

- Layout: run-in paragraphs (no line break per point, items joined by •) at 5.7pt so every line is full.
- Page 1: W1 projects and success; W2 lifecycle, methodologies, requirements, charter, stakeholders; W3 scope; W3–4 schedule (CPM, PERT, compression); W4 cost and EVM; W5 quality; W6 resources and teams; question-bank answer skeletons Q1–Q24.
- Page 2: W7 risk (EMV); W8 procurement; W9 leadership, governance, alignment; W10 integration and change management; W11–12 ITSM and ITIL 4 (SLM, availability); question-bank answers (Q6, Q26–28); ITSM quick distinctions; practice exam with full answers to all 11 parts, plus likely variants.

Sources: INFO6007 lecture slides W1–W12, tutorial answer sheets, the S2 2026 practice exam and the scenario question bank.
