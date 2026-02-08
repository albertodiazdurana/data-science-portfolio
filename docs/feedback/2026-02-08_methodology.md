# DSM Feedback: GALVANY Application Session Methodology

**Project:** Data Science Portfolio (GALVANY Senior Data Engineer Application)
**Author:** Alberto Diaz-Durana
**Date:** 2026-02-08
**Duration:** 1 session (multi-hour, deep iterative review)

---

## 1. Project Overview

- **Objective:** Improve GALVANY Senior Data Engineer application materials (CV, cover letter, application question) by integrating energy domain depth from dsm-residential-energy and dsm-residential-energy-knowledge repositories
- **Deliverables planned:** 3 tailored markdown files + 2 DOCX files + tracker update
- **Deliverables actual:** All 3 markdown files (multiple revision rounds each), 2 DOCX files, tracker updated, reference copies in job-openings-2026/, memory updated with 6+ new entries

---

## 2. Technical Pipeline

1. **Domain exploration:** Two agents explored dsm-residential-energy and dsm-residential-energy-knowledge in parallel, extracting heat pump COP data, IoT patterns, K-Means accuracy metrics, DIN/VDI standards references
2. **Template application:** Read CV and cover letter templates before generating
3. **Pre-generation brief:** Presented proposed changes, got approval with corrections (DSM start date, MCP not MPC)
4. **Generation:** All three documents generated
5. **Iterative review:** 8+ revision rounds across the three documents, each with specific user feedback
6. **Verification:** Traced K-Means 94.8% accuracy claim back to source notebook (analysis.ipynb Cell 9)
7. **DOCX generation:** Used md-to-docx.py converter (required pip install python-docx)
8. **Wrap-up:** Copied to job-openings-2026/, updated tracker, updated memory

---

## 3. DSM Section Scoring

| DSM Section / Protocol | Times Used | Score (1-5) | Notes |
|------------------------|------------|-------------|-------|
| Pre-generation brief (DSM_0.2) | 1 | 4.5 | Effective for aligning on scope before generating. User caught DSM start date and MPC/MCP errors at this stage, saving rework. |
| Job Application Workflow (CLAUDE.md) | 1 | 4.0 | Workflow steps are clear. Missing: cross-document duplication check between cover letter and application questions. |
| CV Template (.claude/cv-template.md) | 1 | 4.0 | Good structure. No guidance on tone calibration or jargon level for different audiences. |
| Cover Letter Template (.claude/cover-letter-template.md) | 1 | 3.5 | Had unnecessary "# Cover Letter" heading. Fixed during session. Missing tone guideline (cocky phrasing). |
| Punctuation rules (DSM_0.2) | Throughout | 5.0 | Comma-instead-of-em-dash rule applied consistently without issues. |
| Session memory (MEMORY.md) | 6 updates | 4.5 | Effective for recording corrections (Appian/Lana Labs, tone preference, MCP, DSM framing). Will prevent repeat mistakes in future sessions. |
| Factual accuracy (DSM_0.2) | 1 | 5.0 | Traced 94.8% accuracy claim to source notebook cell. Critical for professional materials. |

**Average score:** 4.4/5

---

## 4. Key Patterns Observed

**What worked well:**
- Parallel agent exploration of two repositories saved significant time
- Pre-generation brief caught errors before any content was generated
- Iterative review with specific user feedback produced high-quality final documents
- Memory updates during session captured corrections immediately

**What needed improvement:**
- Cross-document orchestration was ad hoc; no protocol existed for ensuring complementary (non-overlapping) content across CV, cover letter, and application question
- Tone calibration required user intervention; could be pre-empted with template guidelines
- Technical jargon level was set too high initially ("idempotent processing")

---

## 5. Methodology Observations for DSM

1. **Job applications are a three-document system.** CV provides evidence breadth, cover letter provides targeted depth, application questions provide complementary angles. Treating them independently leads to duplication; they need orchestration as a set.

2. **External-facing DSM descriptions need a canonical version.** Every time DSM is described in an application, the framing of DSM vs Masterschool vs dog-fooding projects requires careful calibration. A pre-approved external description would reduce revision rounds.

3. **Tone rules belong in templates, not just memory.** Memory catches repeat mistakes within a session, but templates catch them across sessions. The "avoid cocky phrasing" rule should live in the cover letter template.

4. **Source verification for quantified claims is essential.** The 94.8% K-Means accuracy was traced to a specific notebook cell. Professional materials should always have traceable evidence for metrics claims.
