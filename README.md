# ECE 2207 — Electrical Machines I · Study Vault

> **RUET · 2nd Year, 2nd Term · 3 Credits**
> Covers **Transformers**, **3-φ Induction Motors**, and **1-φ Induction Motors**.

---

## What's in This Repo?

A self-contained Obsidian-compatible study vault built from **7 years of past papers**, **3 textbooks**, **11 faculty lecture slides**, **18 class notes**, **85 YouTube lectures**, and **4 class tests** — all digitized, cross-referenced, and analyzed.

---

## Question Analysis at a Glance

> Full analysis → [`ECE_2207_Question_Analysis.md`](ECE_2207_Question_Analysis.md)

### Exam Format

| | 2017–2021 (Old) | 2023–2024 (OBE) |
|:--|:--|:--|
| **Total Marks** | 72 (8 × 12) | 60 (8 × 10) |
| **Attempt** | 6 of 8 (3 per section) | Same |
| **Sections** | A = Transformer, B = Induction Motor | Same |

### The 6 Questions That Never Miss 🔥

These appeared in **5+ out of 7 papers**. Expect them on your exam:

| Topic | Appearances | Section |
|:------|:-----------:|:-------:|
| **OC & SC Test** → parameters, efficiency, regulation | **7/7** | A |
| **Open-Δ** → prove 57.7% capacity | 7/7 | A |
| **Voltage Regulation** derivation (lag / lead / unity) | 5/7 | A |
| **Rotating Magnetic Field** proof ($\Phi_R = 1.5\Phi_m$) | 5/7 | B |
| **DFRT** (Double Field Revolving Theory) for 1-φ IM | 5/7 | B |
| **1-φ IM Starting Methods** (split-phase, capacitor-start, etc.) | 6/7 | B |

### Copy-Paste Numericals

The examiner recycles data. These **identical** problems appeared across papers:

- **20 kVA, 2400/240V OC/SC test** → 2018, 2021
- **No-load: 220V/110V, 0.5A, 30W** → 2020, 2024
- **Scott: 3300V→440V, 33 KVA** → 2018, 2024
- **8-pole, 50Hz, slip 2%: Tmax/Tf ratio** → 2017, 2019 (variant in 2024)
- **IM as IG: 440V, 4-pole, 1470 rpm** → 2018, 2024

> Solve every unique numerical from the 7 papers (~20 problems) and you'll almost certainly see something identical in the exam.

### Trends Worth Watching

| ↑ Rising | ↓ Declining | ⚠️ Syllabus Gap |
|:---------|:------------|:----------------|
| Induction Generator (back in '23 + '24) | Circle Diagram (absent since '21) | 1-φ IM Equivalent Circuit (never asked) |
| "Justify" style open-ended questions | Plugging/braking definitions | Effect of R₂/X₂ on T-s curves |

### Preparation Tiers

| Tier | What | Count |
|:-----|:-----|:-----:|
| 🔵 **FOUNDATION** | Core fundamentals — materials, EM laws, magnetic circuits, per-unit | 1 |
| 🔴 **MUST** | OC test, SC test, Open-Δ, RMF, VR, DFRT, 1-φ starting methods | 7 |
| 🟠 **HIGH** | EMF equation, no-load operation, phasor under load, eq. circuit, efficiency, slip, IM eq. circuit, starting torque, running torque, T-s curves, no-load test, blocked rotor, circle diagram, braking, misc. IM | 15 |
| 🟡 **MEDIUM** | 3-φ connections, Scott/T, vector groups & parallel, auto-transformer, power flow, starting methods (3-φ), induction generator | 7 |
| 🟢 **BONUS** | Construction & core, misc. transformer | 2 |

> Counts are generated from [`boss_notes/00_Index.md`](boss_notes/00_Index.md) and sum to 32 topics.

---

## Repo Navigation

### 🏆 Boss Notes — Your One-Stop Exam Prep

> **This is what you should read.** Everything else in this repo is source material. The boss notes are the final, distilled output.

**32 exam-optimized study notes** covering every topic in the syllabus — built from all the textbooks, slides, class notes, YouTube lectures, and 7 years of past papers. Each note has clear explanations, derivations, diagrams, and the most likely exam questions with solutions.

| | |
|:--|:--|
| 📖 **[Boss Notes Index](boss_notes/00_Index.md)** | Full topic list with priority tags, study plans, and exam predictions |
| 🌱 **[T-00: Start Here](boss_notes/T-00_Core_Fundamentals.md)** | Gentle warm-up on the fundamentals before diving into course topics |
| 📋 **[Formula Sheet](boss_notes/99_Master_Formula_Sheet.md)** | Every formula in one page for last-minute revision |
| 📂 **[boss_notes/](boss_notes/README.md)** | All 32 notes + diagrams |

### 📋 Indexes & Guides

| File | What It Does |
|:-----|:-------------|
| [`Syllabus.md`](Syllabus.md) | Official course syllabus — 3 chapters |
| [`ECE_2207_Question_Analysis.md`](ECE_2207_Question_Analysis.md) | 7-year question analysis: heatmaps, golden questions, predictions |
| [`Topic_Subtopic_Master_List.md`](Topic_Subtopic_Master_List.md) | All 103 subtopics with priority tags, slide refs, and book refs |

### 📖 Source Materials

| Directory | Contents | Count |
|:----------|:---------|:-----:|
| [`Books/`](Books/README.md) | Digitized textbooks — Theraja (Ch-32, 34, 35), Chapman (Ch-1, 2, 4, 7, 10), V.K. Mehta (Ch-7, 8, 9). Each has a topic index. | 20+ files |
| [`SlidesByMaam/`](SlidesByMaam/map.md) | Faculty lecture slides (L-01 to L-11) + [`map.md`](SlidesByMaam/map.md) with slide-by-slide breakdown | 11 lectures |
| [`ClassNoteByRaidah/`](ClassNoteByRaidah/00_Index_and_Topic_Map.md) | Digitized handwritten class notes showing teacher emphasis + [`00_Index_and_Topic_Map.md`](ClassNoteByRaidah/00_Index_and_Topic_Map.md) | 18 classes |
| [`Ankit_Goyal_YT_Playlist/`](Ankit_Goyal_YT_Playlist/00_yt_study_guide.md) | 85 YouTube lectures (GATE-style) with keyframes + [`00_yt_study_guide.md`](Ankit_Goyal_YT_Playlist/00_yt_study_guide.md) for topic lookup | 85 lectures |

### 📝 Exam Papers & Answers

| Directory | Contents |
|:----------|:---------|
| [`PrevYearQuestions/`](PrevYearQuestions/README.md) | 7 past papers (2017–2024, missing 2022) — verbatim question transcripts |
| [`answers_exam_style/`](answers_exam_style/README.md) | Year-wise model answers — exam-ready format (concise, step-by-step, mark-aligned) |
| [`answers_explanation/`](answers_explanation/README.md) | Year-wise detailed explanations — teaches the *why* behind every step |
| [`topicwise_answers_exam_style/`](topicwise_answers_exam_style/README.md) | 25 topic files (T-01 to T-25) — all past questions on a topic grouped with exam-style answers |
| [`topicwise_answers_explanation/`](topicwise_answers_explanation/README.md) | 25 topic files (T-01 to T-25) — same grouping but with deep explanations |
| [`CT_Questions/`](CT_Questions/README.md) | 4 class tests (CT-01 to CT-04) from Session 2023-24 with solutions |

### Quick Lookup — "Where Do I Find…?"

| I need… | Go to |
|:--------|:------|
| Theory or derivation for a topic | `Books/` → use the chapter index files |
| What the teacher emphasized | `SlidesByMaam/map.md` or `ClassNoteByRaidah/00_Index_and_Topic_Map.md` |
| Practice a specific past paper | `PrevYearQuestions/YYYY.md` → then `answers_exam_style/YYYY_answer.md` |
| All past questions on OC/SC test | `topicwise_answers_exam_style/T-06_OC-SC_Tests_Efficiency_and_Losses.md` |
| Intuitive explanation + worked problems | `Ankit_Goyal_YT_Playlist/00_yt_study_guide.md` → find the lecture |
| Exam pattern and predictions | `ECE_2207_Question_Analysis.md` → Sections 10–12 |
| Topic priority before studying | `Topic_Subtopic_Master_List.md` → look at the 🔴/🟠/🟡/🟢 tags |
| Class test questions & solutions | `CT_Questions/` → CT_01 through CT_04 |

---

## Topic File Naming (T-01 to T-25)

Both `topicwise_answers_exam_style/` and `topicwise_answers_explanation/` use the same T-## scheme:

| # | Topic |
|:--|:------|
| T-01 | Transformer Fundamentals & EMF Equation |
| T-02 | Transformer Construction & Core |
| T-03 | No-Load Operation & Phasor Diagrams |
| T-04 | Equivalent Circuit |
| T-05 | Voltage Regulation |
| T-06 | OC/SC Tests, Efficiency & Losses |
| T-07 | Three-Phase Connections & Open-Delta |
| T-08 | Scott (T-T) Connection |
| T-09 | Vector Groups & Parallel Operation |
| T-10 | Auto-Transformer |
| T-11 | Miscellaneous Transformer Topics |
| T-12 | Rotating Magnetic Field |
| T-13 | Slip, Synchronous Speed & Basics |
| T-14 | IM as Rotating Transformer |
| T-15 | IM Equivalent Circuit |
| T-16 | Torque Equations & Characteristics |
| T-17 | Power Flow & Rotor Power |
| T-18 | IM Testing & Circle Diagram |
| T-19 | Starting Methods (3-φ IM) |
| T-20 | Speed Control & Braking |
| T-21 | Induction Generator |
| T-22 | Single-Phase IM Theory (DFRT) |
| T-23 | Single-Phase IM Starting Methods |
| T-24 | Single Phasing |
| T-25 | Miscellaneous IM Topics |
