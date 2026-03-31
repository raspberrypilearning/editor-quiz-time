<h2 class="c-project-heading--task">Add a score</h2>

### Step 1
Add a score display to the page header so the quiz can show the player's points.

<div class="c-project-code">

--- code ---
---
language: html
filename: index.html
line_numbers: true
line_number_start: 11
line_highlights: 13
---
    <header class="header">
      <span class="sitename">Wildlife quiz</span>
      <span id="scoreText" class="sitename">Score: 0</span> <!-- Start the score display at zero. -->
    </header>
--- /code ---

</div>

<div class="c-project-output">
  <p>The header now shows Score: 0 next to your quiz title.</p>
</div>

### Step 2
**Test:** Click **Run**.

You should see **Score: 0** in the header next to your quiz title.
