---
layout: default
title: Live Workshop Hub | 2026 NASW Iowa Symposium
---

<div class="form-card">
  <h2>Live Feedback Terminal</h2>
  <p>Select a discussion section and type your bullet point below. Submitting will save your input anonymously and keep your keyboard ready for the next thought.</p>

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

<script>
  document.addEventListener("DOMContentLoaded", function() {
    const form = document.getElementById("workshopForm");
    const commentInput = document.getElementById("commentInput");
    const statusMessage = document.getElementById("statusMessage");
    const submitBtn = document.getElementById("submitBtn");

    // REPLACE THIS URL with your headless form endpoint (Formspree, Netlify, or custom webhook)
    const ENDPOINT_URL = "https://formspree.io/f/your_form_id";

    form.addEventListener("submit", function(event) {
      event.preventDefault();
      
      const formData = {
        section: document.getElementById("sectionSelect").value,
        comment: commentInput.value,
        timestamp: new Date().toISOString()
      };

      submitBtn.disabled = true;
      statusMessage.textContent = "Sending...";
      statusMessage.style.color = "#0056b3";

      fetch(ENDPOINT_URL, {
        method: "POST",
        headers: {
          "Content-Type": "application/json",
          "Accept": "application/json"
        },
        body: JSON.stringify(formData)
      })
      .then(response => {
        if (response.ok) {
          statusMessage.textContent = "Saved.";
          statusMessage.style.color = "#28a745";
          commentInput.value = "";
          
          // Soft UI Focus-Lock: Keep mobile keyboard active
          setTimeout(() => {
            commentInput.focus();
            statusMessage.textContent = "";
          }, 1200);
        } else {
          throw new Error("Submission failed.");
        }
      })
      .catch(error => {
        statusMessage.textContent = "Error saving. Retry.";
        statusMessage.style.color = "#dc3545";
      })
      .finally(() => {
        submitBtn.disabled = false;
      });
    });
  });
</script>

---

## Active Breakout Prompts

> **Breakout 1: Critical Pedagogy**
> How can field instructors replace "banking model" instruction with dialogue-based problem posing during supervision?

> **Breakout 2: Systems Theory**
> What macro institutional barriers currently prevent non-traditional MSW students from accessing proactive mentorship?

> **Breakout 3: Strengths-Based Action**
> What existing resilient strategies and student-led networks can we formalize into faculty advising frameworks?

---

## Workshop Agenda (90 Minutes)

* **00-15 Min**: Frameworks and EPAS Standards Alignment
* **15-45 Min**: Interactive Small Group Dialogue (Use form above)
* **45-75 Min**: Synthesis of Live Submissions
* **75-90 Min**: Action Planning and CEU Wrap-Up

---

## Detailed Research & Documentation

For full academic papers, CSWE EPAS mapping matrices, and facilitator guides, visit the official [Research Repository](https://github.com/mmonfils/msw-mentorship-support-systems-research).