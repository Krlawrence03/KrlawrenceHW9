# KrlawrenceHW9

A four-page, responsive, accessible web form built with **HTML5**, **CSS3**, **Bootstrap 5.3**, and **Font Awesome**. Deployed as an Azure Static Web App.

## Pages
- `index.html` — Welcome
- `form1.html` — Step 1: Basic info (uses `autofocus`, `required`, email/number validation)
- `form2.html` — Step 2: Preferences (checkbox group required via `required` on the first checkbox; tooltip help; select; textarea)
- `thankyou.html` — Confirmation page with a client-side summary of submitted values

## Best Practices for Forms
- **Clarity & Focus**: 2-step flow with only essential fields to reduce cognitive load and improve completion.
- **Explicit Labels & Grouping**: Each input has `<label for="">`; related inputs use `<fieldset>` + `<legend>` (checkbox group).
- **Validation**: Native HTML5 validation (`type="email"`, `type="number"`, `pattern`, `required`, `min/max`) with accessible hints using `.form-text`.
- **Accessible Help**: Tooltip icon (`fa-circle-question`) provides non-blocking guidance.
- **Clear CTA Language**: Buttons labeled “Continue”, “Submit”, “Start Form” instead of vague “Submit”.
- **Keyboard & Screen Reader Support**: Logical tab order, visible focus styles, ARIA-friendly attributes (`aria-label`, `aria-required`), `aria-live` on summary.

## Accessibility (WCAG 2.1 AA)
- Sufficient color contrast via Bootstrap defaults and custom focus outlines.
- Keyboard navigable components (including tooltips initialized via JS).
- Proper semantics (`<nav>`, `<main>`, `<footer>`, headings, table with scope).
- Form controls associated with labels; groups use `<fieldset>`/`<legend>`.
- Error prevention using native constraints to reduce invalid submissions.

## Running Locally
Open `index.html` in a browser. Navigate through the steps; data is passed via query parameters to `thankyou.html` for a summary.

## Deploying to Azure Static Web Apps
1. Push the project to GitHub (branch `main`).
2. In Azure Portal → *Static Web Apps* → *Create* → Link your GitHub repo (build preset: *Custom*, app location: `/`).
3. After deployment, visit the provided URL and verify all pages.

## Validation
Use:
- W3C HTML Validator – https://validator.w3.org/
- W3C CSS Validator – https://jigsaw.w3.org/css-validator/
- WAVE (WCAG 2.1 AA) – https://wave.webaim.org/

Take screenshots of each pass and compile into a PDF per assignment instructions.
