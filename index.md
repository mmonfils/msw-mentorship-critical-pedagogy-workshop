---
layout: default
title: Live Feedback Terminal | 2026 NASW Iowa Symposium
---

<div class="form-card">
  <h2>Live Feedback Terminal</h2>
  <p>Select a discussion section and type your entry below. Submitting saves your input anonymously and keeps your keyboard active for rapid entries.</p>

  <form id="workshopForm">
    <label for="sectionSelect"><strong>Discussion Section:</strong></label>
    <select id="sectionSelect" name="section" required>
      <option value="Breakout 1: Critical Pedagogy & Banking Models">Breakout 1: Critical Pedagogy & Banking Models</option>
      <option value="Breakout 2: Systems Theory & Institutional Barriers">Breakout 2: Systems Theory & Institutional Barriers</option>
      <option value="Breakout 3: Strengths-Based Mentorship Actions">Breakout 3: Strengths-Based Mentorship Actions</option>
    </select>

    <label for="commentInput"><strong>Your Insight or Note:</strong></label>
    <textarea id="commentInput" name="comment" rows="3" placeholder="Type a bullet point or brief comment..." required></textarea>

    <button type="submit" id="submitBtn">Submit Note</button>
    <span id="statusMessage" class="status-indicator"></span>
  </form>
</div>

---

## Active Breakout Prompts

<div class="breakout-card">
  <h3>Breakout 1: Critical Pedagogy</h3>
  <p>How can field instructors replace "banking model" instruction with dialogue-based problem posing during supervision?</p>
</div>

<div class="breakout-card">
  <h3>Breakout 2: Systems Theory</h3>
  <p>What macro institutional barriers currently prevent non-traditional MSW students from accessing proactive mentorship?</p>
</div>

<div class="breakout-card">
  <h3>Breakout 3: Strengths-Based Action</h3>
  <p>What existing resilient strategies and student-led networks can we formalize into faculty advising frameworks?</p>
</div>

---

## Learning Objectives

{% for obj in site.data.objectives %}
* **{{ obj.title }}** (CSWE EPAS {{ obj.epas }}): {{ obj.description }}
{% endfor %}

---

## Workshop Agenda (90 Minutes)

| Time Window | Duration | Module Title | Format |
| :--- | :--- | :--- | :--- |
{% for item in site.data.agenda -%}
| {{ item.time }} | {{ item.duration }} | {{ item.title }} | {{ item.format }} |
{% endfor %}

---

## Academic Documentation & Research Core

For full theoretical frameworks, CSWE/NASW standards mappings, and empirical research, consult the official [Research Repository](https://mmonfils.github.io/msw-mentorship-support-systems-research/).