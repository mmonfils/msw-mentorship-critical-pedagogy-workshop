# Live Workshop Hub - Technical & Contextual Overview

## Project Identity & Event Context
* **Event**: 2026 NASW Iowa Symposium (Ankeny, Iowa)
* **Session Title**: Mentoring as a Catalyst: Structural Support Systems for MSW Students and Early-Career Practitioners
* **Repository**: `msw-mentorship-support-systems`
* **Published URL**: `https://mmonfils.github.io/msw-mentorship-support-systems/`

## Core Purpose
The Live Workshop Hub serves as a lightweight, zero-friction, mobile-first feedback terminal for workshop participants. It enables attendees to submit real-time insights during breakout segments without requiring login credentials, account creation, or external application downloads.

## Technical Architecture & UX Standards
* **SSG Engine**: Jekyll (Cayman Theme via `jekyll-remote-theme`).
* **Ingestion Pipeline**: Direct asynchronous `fetch()` POST requests sent directly from `_layouts/default.html` to the Airtable Web API endpoint.
* **Network & Load Resilience**: Designed for high-occupancy conference Wi-Fi networks. Operates without heavy JavaScript frameworks, external analytics, or tracking telemetry (`credentials: "omit"`).
* **Accessibility & Form Constraints**:
  * Input text areas enforce `font-size: 16px !important` to eliminate forced viewport zooming on mobile iOS devices.
  * Primary action buttons utilize high-contrast styling and a minimum 48px touch target for accessibility compliance.
  * Soft UI Focus-Lock restores cursor focus to the input box automatically post-submission to support rapid keying.

## Data & Content Synchronization
* **Dynamic Content**: Workshop agenda timelines and learning objectives are rendered dynamically from `_data/agenda.yml` and `_data/objectives.yml`.
* **Cross-Repository Link**: Links directly to the published Research Repository (`https://mmonfils.github.io/msw-mentorship-support-systems-research/`) for comprehensive academic and theoretical documentation.