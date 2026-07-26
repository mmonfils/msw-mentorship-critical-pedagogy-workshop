# CONTEXT.md | MSW Mentorship & Critical Pedagogy Workshop Hub

## Project Identity & Context
* **Event**: 2026 NASW Iowa Symposium
* **Title**: Mentorship as a Catalyst: Exploring Support Systems in Master of Social Work Graduate Training
* **Format**: 90-minute interactive, mobile-first CEU workshop
* **Target Audience**: Social work practitioners, field instructors, academic faculty, and student advocates
* **Core Theoretical Lenses**: Critical pedagogy (Freirean praxis, problem-posing dialogue), economic solidarity, systems theory, CSWE EPAS competencies, and NASW Code of Ethics

---

## Technical Stack & Constraints
* **Platform**: Low-tech static infrastructure hosted on GitHub Pages
* **Theme**: Jekyll Cayman Theme (requires simple, clean layouts)
* **Design Priority**: Mobile-first responsiveness (participants access via mobile browsers during live sessions)
* **Form Integration**: Embedded, responsive Google Form for live group breakout submissions
* **Formatting Guardrails**:
  * Scannable headers and concise bullet points
  * Clean Markdown tables (mobile-friendly width constraints)
  * Accessible typography and high-contrast text layout
  * Plain text ASCII diagrams over heavy media assets

---

## Repository Structure Map

```text
msw-mentorship-critical-pedagogy-workshop/
├── _config.yml               # Jekyll configuration settings
├── _layouts/
│   └── default.html          # Custom or overridden Cayman theme layout
├── assets/
│   └── style.scss            # Custom styling and mobile overrides
├── facilitator/
│   └── index.md              # Facilitator portal: timing, prompts, and talking points
├── research/
│   ├── literature-review.md  # Detailed research literature notes
│   ├── paper-appendices.md   # Appendices for the core research paper
│   └── paper-core.md         # Source of truth: main research paper
├── CONTEXT.md                # Strategic project digest for AI tools and quick orientation
├── favicon.png               # Site favicon
├── index.md                  # Main participant hub: QR code, schedule, breakouts, CEUs
├── LICENSE                   # Open-source license file
├── qrcode.png                # QR code image pointing to live site URL
├── README.md                 # Public repository overview and deployment instructions
├── references.md             # Complete list of 19 academic references
└── thumbnail.jpg             # OpenGraph social card image
```

---

## Core Content & Data Reference

### Workshop Abstract
This presentation explores the critical role of mentorship in Master of Social Work (MSW) education. Grounded in critical pedagogy, the study examines how formal and informal mentoring relationships influence professional identity and academic persistence among emerging practitioners. Findings highlight the need for equitable, developmental support systems that bridge the gap between theory and practice, especially for underserved students.

### Learning Objectives (CEU Aligned)
* **Analyze Mentorship Impact**: Analyze the impact of formal and informal mentorship on professional identity and academic persistence in emerging practitioners.
* **Develop Actionable Models**: Create evidence-based recommendations for designing developmental, rather than administrative, mentorship models in academic and field settings.
* **Examine Reciprocal Growth**: Discuss the reciprocal benefits of the mentoring relationship for both emerging practitioners (mentees) and experienced practitioners (mentors).

### 90-Minute Agenda Structure
* **00:00 - 00:05** (5 min) | Kickoff & Logistics (Facilitator Intro)
* **00:05 - 00:20** (15 min) | Block 1 Briefing: Institutional Guidance (Presentation)
* **00:20 - 00:27** (7 min) | Block 1 Breakout: Discussion & Form Entry (Small Group)
* **00:27 - 00:42** (15 min) | Block 2 Briefing: Non-Traditional Students (Presentation)
* **00:42 - 00:49** (7 min) | Block 2 Breakout: Discussion & Form Entry (Small Group)
* **00:49 - 01:04** (15 min) | Block 3 Briefing: Near-Peer Support (Presentation)
* **01:04 - 01:11** (7 min) | Block 3 Breakout: Discussion & Form Entry (Small Group)
* **01:11 - 01:30** (19 min) | Block 4: Insights & Live Q&A (Large Group Synthesis)

---

## Workflow Instructions for AI Collaborators
1. Treat `research/paper-core.md` as the ultimate source of truth for academic assertions, citations, and theoretical framing.
2. Maintain alignment with CSWE EPAS Competencies (1, 2, 9) and NASW Ethical Standards (1.01, 1.05, 2.05, 3.02).
3. Ensure all proposed UI/UX changes preserve mobile readability on small smartphone displays.