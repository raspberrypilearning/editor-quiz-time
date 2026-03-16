<h2 class="c-project-heading--task">Choose your colours</h2>

--- task ---
Change the quiz colour theme in `default.css` so the page and result box match your chosen style.
--- /task ---

--- task ---
From the file menu, select **default.css**.
--- /task ---

--- task ---
Update the colour variables to choose a new look for your quiz.
You can use [this tool to choose colours](https://www.google.com/search?q=colour+picker)!

--- /task ---


<div class="c-project-code">

--- code ---
---
language: css
filename: default.css
line_numbers: true
line_number_start: 1
line_highlights: 6-12
---
:root {
  /* Font variable */
  --font: 16px/1.25 'Raleway', sans-serif;
  
  /* Base Colours */
  --body-background: #FFFF00; /* Set the page background colour. */
  --background: #33B5E5; /* Set the colour of the header and question cards. */
  --header-font-colour: #ffffff; /* Set the text colour used in the header and result box. */
  --h1-colour: #001e4d; /* Set the dark highlight colour for headings and the result box background. */
  --h2-colour: #001e4d; /* Set the question text colour. */
  --button-background-colour: #ffffff; /* Set the button background colour. */
  --button-font-colour: #001e4d; /* Set the button text colour. */
}
--- /code ---

</div>

<div class="c-project-output">
  <p>Your quiz changes to the bright yellow and blue theme used in the complete example, and the result box text is easy to read.</p>
</div>

--- task ---
**Test:** Click **Run**.

You should see the page colours update, and the text inside the result box should show clearly when you check an answer.
--- /task ---
