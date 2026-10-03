# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## What This Repository Is

An Obsidian-compatible **study vault** for ECE 2207 (Electrical Machine-I) at RUET, 2nd Year 2nd Term. There is no application to build, no test suite, and no linter. The "product" is markdown study notes plus rendered circuit diagrams.

Content covers three chapters only: Transformers, 3-φ Induction Motors, 1-φ Induction Motors (see `Syllabus.md`).

Exam facts that shape almost every file here:
- 8 questions, answer 6 (3 per section). Section A = Transformer (Q1–Q4), Section B = Induction Motor (Q5–Q8).
- 2017–2021 papers: course code ECE **2107**, 72 marks, 12 per question.
- 2023–2024 papers: course code ECE **2207**, 60 marks, 10 per question, CO-mapped (OBE curriculum).
- The 2022 paper is missing and is expected to stay missing.

## Read These First

Per-directory `AGENTS.md` files are the authoritative routing tables. They are **gitignored** (local only), so they will not appear in a fresh clone, but when present they beat anything in this file:

| File | Role |
|:--|:--|
| `.agents/AGENTS.md` | Master query-routing table: "user asks about X, look here first" |
| `.agents/rules/writing_style.md` | **Mandatory** prose rules for all generated content |
| `Books/AGENTS.md` | Topic to textbook-file lookup across Theraja / Chapman / V.K. Mehta |
| `PrevYearQuestions/AGENTS.md`, `CT_Questions/AGENTS.md`, `SlidesByMaam/AGENTS.md`, `ClassNoteByRaidah/AGENTS.md`, `Ankit_Goyal_YT_Playlist/AGENTS.md` | Per-source indexes and lecture/class to topic maps |

## Content Architecture

The vault is a one-way pipeline. Source material flows into analysis, analysis drives derived answers, and everything converges on `boss_notes/`.

```
SOURCES (digitized, read-only in practice)
  Books/               3 textbooks, chapter-split markdown + diagrams/
  SlidesByMaam/        faculty slides L-01..L-11  (see map.md)
  ClassNoteByRaidah/   18 handwritten classes     (see 00_Index_and_Topic_Map.md)
  Ankit_Goyal_YT_Playlist/  85 lectures + frames/ (see 00_yt_study_guide.md)
  PrevYearQuestions/   7 papers, verbatim transcripts
  CT_Questions/        4 class tests, 2023-24 session
        |
        v
ANALYSIS (the single source of truth for priorities)
  ECE_2207_Question_Analysis.md   frequency heatmaps, repeat tracker, predictions
  Topic_Subtopic_Master_List.md   103 subtopics, priority tags, slide + book refs
        |
        v
DERIVED ANSWERS (four parallel views of the same questions)
  answers_exam_style/YYYY_answer.md        concise, mark-aligned
  answers_explanation/YYYY_answer.md       same answers, reasoning spelled out
  topicwise_answers_exam_style/T-NN_*.md   questions regrouped by topic
  topicwise_answers_explanation/T-NN_*.md  same regrouping, explained
        |
        v
FINAL OUTPUT
  boss_notes/   32 distilled notes, the thing a student actually reads
```

`scratch/` holds diagram generator scripts and `_data/` holds archived raw scans. Neither is study material. Never cite them in an answer.

### Two T-numbering schemes exist and they do not match

This is the easiest mistake to make. `topicwise_answers_*/` and `boss_notes/` both use `T-NN` prefixes with **different mappings**:

| | `topicwise_answers_*/` | `boss_notes/` |
|:--|:--|:--|
| Range | T-01 to T-25, flat | T-00 to T-24, with `a`/`b`/`c` splits |
| T-14 | IM as Rotating Transformer | IM Equivalent Circuit |
| T-15 | IM Equivalent Circuit | `T-15a/b/c` Torque (starting / running / curves) |

Resolve `topicwise` numbers against `topicwise_answers_exam_style/README.md` or `Topic_Subtopic_Master_List.md`. Resolve `boss_notes` numbers against `boss_notes/00_Index.md`. Do not translate one to the other by number.

### Priority tags must stay consistent

The 🔴 MUST / 🟠 HIGH / 🟡 MEDIUM / 🟢 LOW tags and the `n/7` exam frequencies all derive from `ECE_2207_Question_Analysis.md`. They are repeated in `Topic_Subtopic_Master_List.md`, `boss_notes/00_Index.md`, each boss note header, and root `README.md`. If a priority changes, update every one of those places.

## Diagrams

### Rules when writing notes

Text-only notes are not acceptable. Every note or answer must embed relevant diagrams.

1. Each content directory carries its **own** `diagrams/` folder. Reference images with a plain relative path: `![caption](diagrams/name.png)`.
2. The same diagram is physically duplicated across directories. `im_blocked_rotor_test_circuit.png` exists in 6 different `diagrams/` folders. Copy the file into the target directory rather than reaching across with `../`.
3. **View the image before embedding it.** Image files are indexed and visible. Confirm the figure actually shows what the surrounding text claims.
4. Source-material figures already carry their own naming conventions: `Ch-32_p05_fig09.jpg` (Theraja), `L-03_ECE-2107_p05_fig01.jpg` (slides), `class04_fig02_twophase_rmf_phasors.jpg` (class notes), `frames/NNN/frame_NNNN_XXmYYs.jpg` (YouTube keyframes).

### Regenerating a circuit diagram

Circuit and phasor diagrams are authored in LaTeX with `circuitikz`, then rasterized. Toolchain required: `pdflatex`, `pdftoppm`, Python with Pillow.

```bash
cd answers_exam_style/diagrams
pdflatex -interaction=nonstopmode transformer_oc_test_circuit.tex
pdftoppm -png -r 300 transformer_oc_test_circuit.pdf transformer_oc_test_circuit_raw
# then whitespace-trim transformer_oc_test_circuit_raw-1.png -> transformer_oc_test_circuit.png
```

The trim step is the `trim()` helper in the `scratch/` scripts (Pillow `ImageChops.difference` against the corner pixel, 25 px margin). `scratch/gen_*.py` and `scratch/generate_*.py` do all three steps in one pass, but they embed **hardcoded absolute `out_dir` paths**, so edit the path before reusing one.

Preamble convention for every diagram (45 cm × 22 cm canvas, trimmed afterwards):

```latex
\documentclass{article}
\usepackage[paperwidth=45cm,paperheight=22cm,margin=10mm]{geometry}
\usepackage{amsmath,amssymb}
\usepackage{tikz}
\usepackage[american]{circuitikz}
\usetikzlibrary{arrows.meta,calc,positioning}
\pagestyle{empty}
```

### Only the PNGs are committed

`.gitignore` excludes `**/*.tex`, `**/diagrams/*.pdf`, `**/*_raw-*.png`, and `scratch/`. The rendered `.png` is the tracked artifact. A `.tex` source may therefore be missing for a diagram that exists, in which case re-author it rather than assuming it was deleted by mistake. Also excluded: `AGENTS.md` at any depth, `.agents/`, `.agentsignore`, `**/.obsidian/`, and `Books/**/*.pdf` (copyrighted textbook scans, never push these).

## Writing Conventions

Follow `.agents/rules/writing_style.md` for all prose. Short sentences, under 20 words where possible. No em-dashes. Plain words. Banned: delve, tapestry, landscape, foster, leverage, nuanced, multifaceted, holistic, pivotal, robust, seamlessly, cornerstone, overarching, transformative, "it is important to note", "plays a crucial role".

Markdown conventions in use:
- Math is LaTeX: `$R_c$` inline, `$$...$$` display, `$$\boxed{...}$$` for results worth remembering.
- Obsidian callouts: `> [!success]`, `> [!example]`, `> [!info]` are the common three.
- Cross-file links are **relative markdown** paths, not wiki links. `[[...]]` appears only as intra-file anchors inside `Ankit_Goyal_YT_Playlist/Lecture_*.md` tables of contents.
- Every boss note opens and closes with a nav line: `[← prev](...) | [🏠 Index](00_Index.md) | [next →](...)`.
- Boss note header block carries `> **Section:** | **Priority:** | **Exam Frequency:**` then a `> **Sources:**` line citing specific articles, for example `Theraja Ch-32 (Art. 32.23–32.25), VK Mehta Ch-7 (Art. 7.18–7.19), Slides L-10 S17`.
- Boss note body order: Why This Topic Matters, Key Definitions (quoted from a named source), theory and derivations, 🏆 Golden Questions (with the year and mark value it appeared for), ⚡ Exam Tips & Common Mistakes, 🔗 Related Topics.
- Quote definitions verbatim and attribute them. Cite the file and section when answering a question.

## Constraints

- Stay inside `/home/azaz/AntigravityxStudy/SemesterFinal_2_2/ECE_2207`. Do not read or write outside it.
- `.agentsignore` keeps raw page dumps, PDFs, and digitizer manifests out of context. All `.md` and all image files stay visible. Do not index `**/*_Pages/`, `**/pdf/pages/`, `SlidesByMaam/pdfs/`, or `_data/`.
- Adding a new topic file means updating its directory `README.md`, the relevant index (`boss_notes/00_Index.md` or the topicwise README), and root `README.md` if the navigation table changes.
