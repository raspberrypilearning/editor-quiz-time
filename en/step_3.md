<h2 class="c-project-heading--task">Choose your colours</h2>

### Step 1
Change the quiz colour theme in `default.css` so the page and result box match your chosen style.

### Step 2
From the file menu, select **default.css**.

### Step 3
Update the colour variables to choose a new look for your quiz.
You can copy this example or pick your own colours.
You can use [this tool to choose colours](https://www.google.com/search?q=colour+picker){:target="_blank"}!



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
  --body-background: #F4F1DE; /* Set the page background colour. */
  --background: #2A9D8F; /* Set the colour of the header and question cards. */
  --header-font-colour: #ffffff; /* Set the text colour used in the header and result box. */
  --h1-colour: #264653; /* Set the dark highlight colour for headings and the result box background. */
  --h2-colour: #ffffff; /* Set the question text colour. */
  --button-background-colour: #E9C46A; /* Set the button background colour. */
  --button-font-colour: #264653; /* Set the button text colour. */
}
--- /code ---

</div>

<div class="c-project-output">
  <p>Your quiz changes to the colours you choose, and the result box text is easy to read.</p>
</div>

### Step 4
**Test:** Click **Run**.

You should see the page colours update, and the text inside the result box should show clearly when you check an answer.
