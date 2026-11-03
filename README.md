# Search Committee Confidentiality Check

A small, accessible two-question knowledge check for Great Falls College Hiring Training.

## Files

- `activity/index.html` — standalone interactive activity for GitHub Pages
- `canvas-page.html` — revised Canvas page with the new hero-banner design and iframe placeholder
- `.nojekyll` — prevents GitHub Pages from trying to process the project with Jekyll

## Accessibility and design

- Uses a restrained Great Falls College-style palette.
- Text/background combinations are designed around a 6:1 contrast target or higher.
- Confetti is disabled automatically when the learner has `prefers-reduced-motion` enabled.
- Sound is OFF by default and only starts after learner interaction.
- No audio file is required; the success tone is generated in the browser.
- Keyboard focus is visible.
- Feedback uses `aria-live`.
- The confidentiality graphic on the Canvas page uses `alt=""` because the same information is provided in nearby HTML.

## Publish with GitHub Pages

1. Create a new GitHub repository named:

   `search-committee-confidentiality-check`

2. Upload the contents of this folder to the repository.

3. In GitHub, open:

   **Settings → Pages**

4. Under **Build and deployment**, choose:
   - Source: **Deploy from a branch**
   - Branch: **main**
   - Folder: **/ (root)**

5. Save.

6. Your site will publish at something like:

   `https://YOUR-GITHUB-USERNAME.github.io/search-committee-confidentiality-check/`

7. The activity URL will be:

   `https://YOUR-GITHUB-USERNAME.github.io/search-committee-confidentiality-check/activity/`

## Connect it to Canvas

Open `canvas-page.html` and replace:

`https://YOUR-GITHUB-USERNAME.github.io/search-committee-confidentiality-check/activity/`

with your actual GitHub Pages activity URL.

Then paste the contents of `canvas-page.html` into the Canvas HTML editor.

## If Canvas blocks the iframe

Use the GitHub Pages activity URL as a normal link or button instead. The activity works as a standalone page.

## Editing the activity

Open `activity/index.html`.

Each answer button includes a `data-correct` value:

```html
<button class="option" type="button" data-q="1" data-correct="true">
  Correct answer text
</button>
```

Change the visible answer text freely. Only change `data-correct` if you want a different option to be scored as correct.

Feedback text is stored in the `feedbackText` JavaScript object.

## Important limitation

This activity gives immediate feedback, confetti, and optional sound, but it does not write a score to the Canvas Gradebook. A graded result would require a Canvas quiz, LTI, SCORM-style package, or another integration.
