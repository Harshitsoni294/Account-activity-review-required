Instagram "Forgot password" clone

This repository contains a static HTML/CSS clone of Instagram's "Trouble with logging in?" page as shown in the provided screenshot. It's intended as a small internship/project piece.

What is included

- `index.html` — page markup (static). The Instagram-style logotype and lock icon use web fonts / inline SVG so no external image files are required.
- `styles.css` — styles that recreate the dark theme, centered card, input and button.

How to run (Windows PowerShell)

1. Open PowerShell and change directory to this project folder, for example:

```powershell
cd "c:\Users\harsh\OneDrive\Desktop\My projects\insta"
```

2. Start a simple HTTP server (Python 3 must be installed):

```powershell
python -m http.server 8000
```

3. Open your browser and navigate to `http://localhost:8000`.

Notes & next steps

- The page is static; the form submit handlers only show a placeholder alert. Add your backend endpoints if you want to connect it.

- The recover form has been wired to Formspree using the form ID `mrblvqpv`. Submissions to the "Send login link" button POST to https://formspree.io/f/mrblvqpv and Formspree will forward the received fields (the phone number field is named `phone`) to the configured email address on that Formspree form.
- To test: run the server, submit a phone number, and check the email inbox configured for the Formspree form. Formspree may require confirming the sender/email depending on your Formspree account settings.
- Replace the fonts or tweak colors to match the screenshot perfectly; fonts may appear slightly different across platforms.
- If you'd like, I can add a mobile-optimized variant, or export a small screenshot-compare test using Playwright/puppeteer.
