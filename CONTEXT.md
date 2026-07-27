---
layout: default
title: Context | MSW Mentorship & Critical Pedagogy Workshop Hub
---

# CONTEXT.md | MSW Mentorship & Critical Pedagogy Workshop Hub

## Project Identity & Metadata
* **Title**: Mentorship as a Catalyst: Exploring Support Systems in Master of Social Work Graduate Training
* **Event**: 2026 NASW Iowa Symposium
* **Target Audience**: Social work practitioners, field instructors, academic faculty, and student advocates
* **Workshop Format**: 90-minute interactive, mobile-first CEU workshop
* **CEU Focus**: Supporting licensed social workers in meeting CSWE and NASW standards through developmental mentorship practices

## Theoretical & Analytical Lenses
The workshop content and structure are grounded in the following academic frameworks:
* **Critical Pedagogy (Freirean Praxis)**: Utilizing dialogue and problem-posing education to empower students and challenge traditional "banking" models of instruction.
* **Systems Theory (Person-in-Environment)**: Analyzing the MSW student experience within the context of institutional barriers, remote learning environments, and competing life roles.
* **Economic Solidarity**: Designing near-peer support models that avoid the exploitation of "unpaid emotional labor" while fostering horizontal networks of mutual learning.
* **Proactive Mentorship**: Shifting the burden of persistence from the student to the institution through automated or embedded support systems.

## Standards & Ethics Alignment
Content is mapped to specific professional standards to ensure CEU eligibility:
* **CSWE EPAS Competencies**:
    * **Competency 1**: Demonstrate Ethical and Professional Behavior
    * **Competency 2**: Advance Human Rights and Social, Racial, Economic, and Environmental Justice
    * **Competency 9**: Evaluate Practice with Individuals, Families, Groups, Organizations, and Communities
* **NASW Code of Ethics**:
    * **Standard 1.01**: Commitment to Clients (Professional Integrity)
    * **Standard 1.05**: Cultural Competence and Social Diversity
    * **Standard 2.05**: Consultation (Inter-professional Collaboration)
    * **Standard 3.02**: Education and Training (Responsibility of Educators/Field Instructors)

## Source of Truth Reference Map
The following file serves as the ultimate authority for all academic assertions, research findings, and theoretical citations:
* **Primary Authority**: `research/paper-core.md`
* **Role**: All focus questions, "Research Context" snippets in the breakout cards, and workshop abstract content must derive directly from the data and analysis presented in this core paper.

## Jekyll Data & Site Architecture
The site utilizes Jekyll's data folder to maintain synchronization across multiple pages:
* **_data/agenda.yml**: The single source of truth for the workshop timeline. Used in `index.md` and `facilitator/index.md` via Liquid {% raw %}`{% for item in site.data.agenda %}`{% endraw %} loops to ensure timing and block titles match.
* **_data/objectives.yml**: Contains title, EPAS mapping, and descriptions for CEU goals, rendered as a list in the Hub.
* **index.md (The Hub)**: The participant-facing landing page containing the QR code, active breakout prompts, and the embedded Google Form.
* **facilitator/index.md (Facilitator Portal)**: Contains detailed briefing notes and a direct link to the Live Google Form Summary View for real-time data synthesis.

## Mobile UI & Technical Guardrails
To ensure maximum accessibility on mobile devices during the symposium, the following technical constraints are enforced:
* **Base Theme**: Jekyll Cayman Theme (minimalist, high-contrast, responsive).
* **UI Structure**: Use of the `.breakout-card` CSS class for all discussion prompts and agenda items to provide clear visual containers.
* **Google Form Integration**: Embedded via `<iframe>` with 100% width and fixed height (846px) to minimize scrolling friction within the page.
* **Formatting Restrictions**:
    * No emojis: Maintain a professional, academic aesthetic.
    * No em dashes: Use standard punctuation or hyphens to ensure uniform rendering across various mobile browsers.
    * Plain Text Diagrams: Use ASCII-based flowcharts to ensure structural clarity without requiring heavy image assets.
* **Navigation**: Relative paths must be used (e.g., `./facilitator/`) to ensure the site remains functional across local testing and GitHub Pages deployment.