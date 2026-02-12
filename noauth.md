# No auth

Exercise 2 — “Steal money from others” (No Auth Checks)
Goal: Pretend to be another user and access or operate on their account.

Mindset to teach

“How does the app decide who I am?”
“Can I change that identity?”
Step‑by‑step hints (progressive)

Observe: After login, what changes? (Any session values? Cookies? URLs?)
Trace: Find where the dashboard or transfer uses your identity. (What parameter or stored value is used?)
Experiment: Open two accounts in different browsers or a private window. Compare requests.
Hypothesis: If identity is stored in a simple value, can you change it?
Test small: Try changing only one thing at a time (a cookie value, a query param, or a form field).
Watch the effect: Do you see another user’s data or send a transfer on their behalf?
Reflection: Which missing check made it possible? (Think “authorization,” not “authentication.”)
Guidance to avoid “all answers”

Ask them to locate the single point where the app picks “who is current user.”
Then ask: “What if I can alter that value?”