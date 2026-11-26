---
title: "e-Learning"
---
<style>
/* Course cards: thumbnail, description, and a button that opens the course full screen. */
.course-card {
  display: grid;
  grid-template-columns: minmax(0, 300px) minmax(0, 1fr);
  gap: 24px;
  align-items: start;
  margin: 14px 0 8px;
}
.course-thumb {
  display: block;
  border: 1.5px solid var(--line);
  border-radius: var(--radius);
  overflow: hidden;
  background: var(--card);
  transition: transform .12s ease, box-shadow .12s ease;
}
.course-thumb:hover { transform: translate(-3px, -3px); box-shadow: var(--shadow-hover); }
.course-thumb img { display: block; width: 100%; height: auto; aspect-ratio: 8 / 5; }
.course-card p { margin-top: 0; }
.course-open {
  display: inline-flex; align-items: center; gap: 10px; padding: 12px 24px; margin-top: 4px;
  background: var(--accent-strong); color: #fff; font-family: var(--font-display);
  font-weight: 800; font-size: 16px; border: 1.5px solid var(--line);
  border-radius: var(--radius-button); text-decoration: none;
  transition: transform .12s ease, box-shadow .12s ease;
}
.course-open:hover { background: var(--accent-strong-hover); color: #fff; transform: translate(-3px, -3px); box-shadow: var(--shadow-hover); }
@media (max-width: 640px) {
  .course-card { grid-template-columns: 1fr; gap: 14px; }
}
</style>

I build self-paced e-learning courses that teach people how to set up and get the most out of PagerDuty. Each course is fully interactive and opens full screen in a new tab.

<div class="desktop-note" role="note"><svg viewBox="0 0 24 24" width="26" height="26" fill="none" stroke="#36677a" stroke-width="1.8" stroke-linecap="round" stroke-linejoin="round" aria-hidden="true"><rect x="3" y="4" width="18" height="12" rx="2"/><path d="M2 20h20"/></svg><p><strong>Best on a computer.</strong> These interactive courses are built for a larger screen. On a phone they won’t display the way they’re meant to, so open them on a desktop or laptop for the full experience.</p></div>

### Escalation Policy Basics

<div class="course-card">
  <a class="course-thumb" href="../elearning/escalation-policy-basics/" target="_blank" rel="noopener" aria-label="Open Escalation Policy Basics full screen">
    <img src="escalation-policy-basics-thumb.jpg" alt="Opening screen of the Escalation Policy Basics course" width="800" height="500" loading="lazy">
  </a>
  <div>
    <p>Escalation policies decide who gets notified, in what order, and what happens when nobody answers. This course covers how incidents move through escalation levels, how to choose targets and set timeouts, how to plan on-call handoffs, and which common anti-patterns to avoid.</p>
    <a class="course-open" href="../elearning/escalation-policy-basics/" target="_blank" rel="noopener">Open the course ↗</a>
  </div>
</div>

---

### Notification Rules & User Profiles

<div class="course-card">
  <a class="course-thumb" href="../elearning/notification-rules-user-profiles/" target="_blank" rel="noopener" aria-label="Open Notification Rules and User Profiles full screen">
    <img src="notification-rules-user-profiles-thumb.jpg" alt="Opening screen of the Notification Rules and User Profiles course" width="800" height="500" loading="lazy">
  </a>
  <div>
    <p>When an incident is assigned to you, your user profile decides how and when PagerDuty reaches you. This course walks through each profile tab, adding and testing contact methods, configuring notification rules for high- and low-urgency incidents, and managing account settings.</p>
    <a class="course-open" href="../elearning/notification-rules-user-profiles/" target="_blank" rel="noopener">Open the course ↗</a>
  </div>
</div>

---

### PagerDuty's AI Capabilities

<div class="course-card">
  <a class="course-thumb" href="../elearning/pagerduty-ai/" target="_blank" rel="noopener" aria-label="Open PagerDuty's AI Capabilities full screen">
    <img src="pagerduty-ai-thumb.jpg" alt="Opening screen of the PagerDuty's AI Capabilities course" width="800" height="500" loading="lazy">
  </a>
  <div>
    <p>An introduction to the generative and agentic AI built into the PagerDuty platform: the PagerDuty Assistant, the four AI agents, Paige the SRE Agent in action, and how these capabilities are enabled and governed.</p>
    <a class="course-open" href="../elearning/pagerduty-ai/" target="_blank" rel="noopener">Open the course ↗</a>
  </div>
</div>

---

### Your First Tailnet (concept course for Tailscale)

<div class="course-card">
  <a class="course-thumb" href="../elearning/your-first-tailnet/" target="_blank" rel="noopener" aria-label="Open Your First Tailnet full screen">
    <img src="your-first-tailnet-thumb.jpg" alt="Welcome screen of the Your First Tailnet course, with lesson details and a diagram of a laptop and phone connecting to a home server" width="800" height="500" loading="lazy">
  </a>
  <div>
    <p>A self-initiated concept course, built from Tailscale's public docs to show how I'd approach their learning content. It covers what a tailnet is, how devices find each other, direct versus relayed connections, a hands-on setup, and access rules with grants. Includes a design system based on Tailscale's look and a diagram style guide. Not an official Tailscale course.</p>
    <a class="course-open" href="../elearning/your-first-tailnet/" target="_blank" rel="noopener">Open the course ↗</a>
  </div>
</div>
