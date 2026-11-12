---
title: "Programming"
---

I enjoy building things beyond documentation. Here are some projects I made with Claude Code.

### Pub Trivia

<figure class="graphic-embed games-graphic">
  <object data="how-the-games-work.svg" type="image/svg+xml" aria-label="How the games work: the host opens the big screen and gets a room code, and each team joins on a phone. In 6Clues, movie clues appear one at a time and earlier guesses score more. In Pub Trivia, the host builds a quiz from the round bank, teams answer each round on their phone, and the answers are revealed with ticks and crosses.">
    <img src="how-the-games-work.svg" alt="How the games work: a big screen with a room code, team phones, and how 6Clues and Pub Quizzes are played and scored.">
  </object>
</figure>

I used to host pub trivia, including a movie trivia game called 6Clues. I turned all the questions I wrote over the years into two games you can play with friends. The host puts the game on a big screen, and each team joins on a phone with a four-letter room code.

In **6Clues**, each movie is revealed over six clues, hardest first. The earlier your team guesses it, the more points you earn. **Pub Trivia** is a classic pub quiz: the host picks tonight's rounds, teams answer each round on their phone, and the big screen reveals the answers one by one.

<div class="game-buttons">
  <a href="https://6clues.netlify.app/" target="_blank" rel="noopener noreferrer">6Clues Trivia ↗</a>
  <a href="https://pub-quizzes.netlify.app/" target="_blank" rel="noopener noreferrer">Pub Trivia ↗</a>
</div>

<style>
.games-graphic { margin: 8px 0 28px; padding: 0; overflow: hidden; background: #f6f1ea; }
.games-graphic object, .games-graphic img { display: block; width: 100%; height: auto; aspect-ratio: 1200 / 1120; }
.game-buttons { display: flex; flex-wrap: wrap; gap: 14px; margin-top: 24px; }
.game-buttons a {
  display: inline-flex; align-items: center; gap: 10px; padding: 14px 28px;
  background: var(--accent-strong); color: #fff; font-family: var(--font-display);
  font-weight: 800; font-size: 16px; border: 1.5px solid var(--line);
  border-radius: var(--radius-button); text-decoration: none;
  transition: transform .12s ease, box-shadow .12s ease;
}
.game-buttons a:hover { background: var(--accent-strong-hover); transform: translate(-3px, -3px); box-shadow: var(--shadow-hover); }
</style>

### John Lithgow Movie Picker

Pick a John Lithgow movie with the spin of a wheel.

<div style="margin-top: 24px;">
  <a href="https://vrbabapancake.github.io/john-lithgow/" target="_blank" rel="noopener noreferrer"
     style="display:inline-flex;align-items:center;gap:10px;padding:14px 28px;background:var(--accent-strong);color:#fff;font-weight:800;font-size:16px;border-radius:var(--radius-button);text-decoration:none;">
    Spin the Wheel ↗
  </a>
</div>

### Columbo Scenario Creator

Build your own Columbo murder mystery with a few taps. Pick a murderer, a victim, a motive, a murder method and an alibi, then see the slip-up that gives them away, Columbo's "just one more thing" and how he catches them. Every piece comes from the first four seasons of the show, so you can end up with a chess grandmaster killing his rich uncle with exploding cigars to save a vineyard.

<div class="game-buttons">
  <a href="../columbo-scenario-creator/">Create a case →</a>
</div>
