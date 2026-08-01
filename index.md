---
layout: default
title: Live Workshop Feedback Terminal
---

# Live Workshop Terminal

<div class="form-card">
  <h2>Submit Breakout Insight</h2>
  <form id="workshopForm">
    <label for="sectionSelect">Breakout Theme:</label>
    <select id="sectionSelect" name="section" required>
      <option value="Breakout 1: Institutional Guidance & Critical Pedagogy">Breakout 1: Institutional Guidance & Critical Pedagogy</option>
      <option value="Breakout 2: Non-Traditional Students & Institutional Barriers">Breakout 2: Non-Traditional Students & Institutional Barriers</option>
      <option value="Breakout 3: Strengths-Based Mentorship Actions">Breakout 3: Strengths-Based Mentorship Actions</option>
    </select>

    <label for="commentInput">Key Insights / Real-Time Takeaways:</label>
    <textarea id="commentInput" name="comment" rows="4" placeholder="Enter your notes or key takeaways here..." required></textarea>

    <button type="submit" id="submitBtn">Submit Insight</button>
    <span id="statusMessage" class="status-indicator"></span>
  </form>
</div>