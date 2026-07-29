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
* **Strengths-Based Approach**: Identifying and leveraging the inherent assets, experiential knowledge, and resilient coping mechanisms that social work students bring to graduate education and field placements.
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
* **Primary Authority**: `research/paper-core.md` (Migrated to the companion Just the Docs research repository)
* **Role**: All focus questions, breakout card prompts, and workshop abstract content derive directly from the core paper analysis.

## Live Workshop Hub Refactor Architecture
The Live Workshop Hub is a single-page, mobile-first Jekyll site built on the Cayman theme. It operates as a zero-friction input terminal for workshop attendees.

### Tech Stack
* **Frontend**: Single-page Jekyll web application using the responsive Cayman theme.
* **Submission Form**: Native HTML/CSS input fields embedded directly on the page without third-party iframes, cookie banners, or external authentication.
* **Backend Processing**: Headless form handler (Formspree, FormKeep, or Netlify Forms) accepting background data payloads via AJAX/Fetch API.
* **Data Destination**: Submissions pipe automatically from the form backend directly into a live Google Sheet for real-time group synthesis by the facilitator.
* **Documentation Split**: Extensive developer notes, facilitator guides, research files (`research/`), and reference lists (`references.md`) reside in a separate repository powered by the Jekyll "Just the Docs" theme.

## UX Optimization Requirements (No-Friction Blueprint)
1. **Single-Input Stream Workflow**: Attendees submit rapid, bullet-style feedback. The interface consists of a single text field and a section selector (dropdown or radio buttons) to assign thoughts to one of three active discussion prompts.
2. **Background Submission (AJAX/Fetch)**: Submitting data executes asynchronously. Page reloads, site redirects, and "Thank You" confirmation windows are strictly forbidden.
3. **Soft UI Focus-Lock**: Upon successful submission, JavaScript immediately resets the text area, displays a subtle success indicator, and calls `.focus()` on the text field. This keeps the mobile keyboard active for immediate follow-up entries.
4. **Data Privacy Safeguards**: Strict anonymity is maintained. Payloads contain only raw string data (Section Name and Text Input) stripped of tracking cookies, telemetry, or user identifiers.

## Mobile UI & Layout Hierarchy
* **Form-First Viewport Placement**: The interactive HTML form resides at the top of the content area directly beneath the main site header, ensuring immediate access upon scanning the QR code.
* **Below-the-Fold Reference Material**: The condensed 90-minute workshop agenda, active breakout prompts, and CEU criteria sit below the active form block to provide contextual reference without interrupting input flow.
* **CSS Visual Containers**: Breakout prompts and agenda blocks utilize the `.breakout-card` styling class for high-contrast mobile scanning.
* **Formatting Restrictions**:
    * No emojis: Maintains a clean, professional aesthetic.
    * No em dashes: Standard punctuation or hyphens are used exclusively to guarantee consistent mobile browser rendering.
    * Plain Text Diagrams: ASCII flowcharts render structural logic without heavy image payloads.