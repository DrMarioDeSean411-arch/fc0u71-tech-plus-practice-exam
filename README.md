# CompTIA Tech+ (FC0-U71) — Full Practice Exam
## 300 Questions · 50 per Domain · Domain Study Guide + Auto-Graded Practice

> **All auto-graded in the browser. No login required. No installation. Works on any device.**

---

### Live Exam Link

**[https://DrMarioDeSean411-arch.github.io/fc0u71-tech-plus-practice-exam/fc0u71_full_practice_exam.html](https://DrMarioDeSean411-arch.github.io/fc0u71-tech-plus-practice-exam/fc0u71_full_practice_exam.html)**

Bookmark this link. You can return to it at any time — your answers are saved in your browser tab while it stays open (they reset if you close the tab; this tool does not use persistent storage).

---

## What Is This?

This is a full practice bank for the CompTIA Tech+ (FC0-U71) certification exam, built around three views:

1. **Practice Questions** — 300 original multiple-choice questions, an even 50 per domain, each with an immediate rationale and an instructor misconception note.
2. **Domain Study Guide** — a clickable, expandable reference that breaks down every domain's official sub-objectives (1.1, 1.2, 2.1, 2.2...) in plain language, independent of the question bank, for review before or between practice attempts.
3. **Visual Reference** — original inline SVG diagrams (no external images, nothing that can break or go offline) covering Domain 2.0 Infrastructure: a labeled motherboard layout, a grid of port/connector shapes (USB-A/B/C, Thunderbolt, Lightning, RJ45, RJ11, HDMI, DVI, VGA, DisplayPort, SFP), a volatile-vs-non-volatile storage comparison, an Ethernet/fiber cable cutaway plus common tools (crimper, cable tester, ESD wristband), and a small-network topology diagram (modem → router/firewall → switch/access point → devices).

There is **no login, no tracking, and no data sent anywhere** — everything runs entirely in your browser, matching the zero-dependency architecture used across this instructor's other practice tools.

---

## Exam Structure

The real FC0-U71 exam is a maximum of 70 multiple-choice questions in 60 minutes, with a passing score of 650 (on a 100–900 scale). This tool gives an even, deep bank across all six domains regardless of their exam-day weighting, so no domain is under-practiced:

| # | Domain | % of Real Exam | Practice Questions |
|---|--------|-----------------|----------------------|
| 1.0 | IT Concepts and Terminology | 13% | 50 |
| 2.0 | Infrastructure | 24% | 50 |
| 3.0 | Applications and Software | 18% | 50 |
| 4.0 | Software Development Concepts | 13% | 50 |
| 5.0 | Data and Database Fundamentals | 13% | 50 |
| 6.0 | Security | 19% | 50 |
| | **Total** | **100%** | **300** |

Every question is multiple-choice with 4 options, matching the real exam's question format. Because Infrastructure and Security carry the most exam weight, students should not read the even 50/50/50 split as "equal importance" — pace study time toward the real percentages above even though the practice bank itself is flat.

---

## How to Use This Exam

1. Use the **Practice Questions / Domain Study Guide** toggle at the top of the page to switch views.
2. In the **Domain Study Guide**, click any of the six domain cards to expand it and read a plain-language breakdown of every official sub-objective in that domain (for example, 2.1 Computing Devices, 2.2 Internal Components...).
3. In **Practice Questions**, select a domain button to load its 50-question bank, then use the **Q1–Q50** tabs to move between questions.
4. Click an answer. The correct answer, a full rationale, and an instructor misconception note appear immediately.
5. Watch the domain and difficulty breakdown bars at the bottom — anything scoring low needs review before you move on.

> **Recommended approach:** Read a domain's Study Guide entry first, then immediately work that domain's 50 practice questions. Repeat domain by domain, then use the breakdown bars to identify any objective that still needs another pass before scheduling the real exam.

---

## Scoring Guide

The real FC0-U71 exam reports a scaled score out of 900, with a **passing score of 650**. This tool approximates that pass line at a 65% raw score.

| Raw Score | What it means |
|-----------|---------------|
| 90–100% | Exam ready — schedule your assessment |
| 65–89% | Passing range — review weak domains before testing |
| 50–64% | Close — focus study on domains below 65% |
| Below 50% | More preparation needed — revisit the Domain Study Guide |

The breakdown bars at the bottom of the practice page show your score by:
- Each of the six official domains (1.0–6.0)
- Difficulty level (Foundational / Intermediate / Advanced)

Use these, together with the Domain Study Guide, to target remaining study time before attempting the real CompTIA exam.

---

## Domains Covered

**1.0 — IT Concepts and Terminology:** basics of computing (input/processing/output/storage) · binary/hex/decimal/octal notation · storage, throughput, and processing-speed units · troubleshooting methodology

**2.0 — Infrastructure:** common computing devices and IoT · internal components (motherboard, RAM, CPU, GPU, NIC) · storage types · peripheral installation · I/O device interfaces and display ports · virtualization and cloud service/deployment models · internet service types · basic networking concepts · small wireless network capabilities

**3.0 — Applications and Software:** OS components and file management · purpose of operating systems and OS types · productivity, collaboration, and remote-support software · web browser configuration · common uses of AI (chatbots, assistants, generative AI, predictions)

**4.0 — Software Development Concepts:** programming language categories (interpreted, compiled, query, markup) · fundamental data types · variables, constants, arrays, functions, and objects · pseudocode, flowcharting, branching, and looping

**5.0 — Data and Database Fundamentals:** the value of data and information · database concepts and uses · relational vs. non-relational database structures · data backup concepts and locations

**6.0 — Security:** CIA triad and AAA concepts · privacy and PII · securing devices and best practices · password best practices · encryption use cases (data at rest vs. in transit) · small wireless network security configuration

---

## Original Content Notice

All 140 questions, rationales, and instructor misconception notes in this tool were written from scratch to test the objectives published in CompTIA's official *Tech+ FC0-U71 Certification Exam Objectives (Version 2.0)* document. None of the content reproduces or paraphrases actual CompTIA exam questions ("brain dumps"), consistent with CompTIA's Authorized Materials Use Policy.

---

## For the Instructor

The exam is a single self-contained HTML file (`fc0u71_full_practice_exam.html`) with zero external dependencies. All questions, rationale, the domain study guide content, and grading logic are bundled inline — no server, no database, no CDN calls required. GitHub Pages serves it as a static file.

To add or edit **practice questions**, the question bank lives in six arrays near the top of the `<script>` block (`ITC`, `INFRA`, `APPS`, `DEV`, `DATA`, `SEC`), each holding exactly 50 objects with this schema:

```js
{
  "comp": "SEC",                 // domain short code — matches DOMAIN_META keys
  "topic": "Password Best Practices",
  "type": "mc",
  "stem": "Question text...",
  "opts": ["Option A", "Option B", "Option C", "Option D"],
  "ans": 1,                      // zero-indexed correct answer
  "rationale": "HTML string explaining the correct answer",
  "misconception": "Instructor note on the common wrong-answer pattern",
  "diff": "found | inter | adv"
}
```

To edit the **Domain Study Guide**, look for the `STUDY_GUIDE` object, keyed by the same six domain codes. Each domain holds a `label`, a `weight` (its real-exam percentage), and a `subs` array of sub-objective entries (`id`, `title`, `body`) rendered as expandable accordion cards.

Push changes to the `main` branch and GitHub Pages rebuilds automatically within 1–2 minutes.

---

*CompTIA Tech+ (FC0-U71) · Practice exam prepared by Dr. Mario Booker*
