# XSS

TODO: Lägg till message i transfer som visas hos avsändaren och mottagaren separat, så att det bara är i mottagarens vy man skickar skit.

Exercise 1 — “Be annoying to the bank and its customers” (XSS alert)
Goal: Make a pop‑up alert appear for other users by entering a “message” that the site later displays.

Mindset to teach

“Where does my input show up later?”
“Does the site treat my input as text, or as code?”
Step‑by‑step hints (progressive)

Recon: Find any input fields that get displayed later (transfer “message” is a great start).
Confirm reflection: Enter a unique marker like XSS_TEST_123 and check the history list.
Probe formatting: Try characters like < and > in the message. Do they show up as literal text or disappear?
Hypothesis: If the page renders HTML you typed, it may also run scripts.
Minimal test: Try a tiny HTML tag first (e.g., bold text). If it renders as HTML, you’re close.
Next step: Try a very small script‑like payload that should cause a visible effect (e.g., an alert).
Validate: If it fires on reload, you’ve got stored XSS.
Reflect: What made this possible? Identify the exact output location that didn’t escape your input.
Guidance to avoid “all answers”

Have them test one character change at a time.
Encourage them to keep a journal: input → output → hypothesis.