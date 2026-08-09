# ABTalks Redesign

Complete prompt log for the hackathon submission project

---

## 1. Prompt 1 — Initial redesign brief

> https://www.abtalks.in/hackathon/submission
> Rebuild this website, featuring the suggested updates mentioned in the 1st problem statement on this website. The statement is: "Redesign ABTalks (Reimagine the platform you are standing on)."

*Kicked off the project: fetch the live ABTalks site and redesign it against the hackathon's own "redesign ABTalks" problem statement.*

---

## 2. Prompt 2 — Three-screen spec

> Now, this website should have three screens:
>
> 1. Landing page - the first experience for a student who has never heard of ABTalks. Show enough trust, clarity, and motivation that they are willing to commit to a 60-day challenge.
> 2. Student Dashboard - the home screen after logging in. Include essentials such as:
>    a. Current streak
>    b. Today's task
>    c. Progress through the challenge
>    d. Overall completion
>    e. Student standing or achievements
> 3. Challenge day - The complete experience of a single challenge day. Student should be able to:
>    a. Read the day's task
>    b. Understand what needs to be built
>    c. Submit proof of work:
>       i. GitHub repository or commit
>       ii. LinkedIn post
>
> **What We're Looking For**
>
> Your redesign should:
> - Be designed mobile-first (390px), with desktop as a secondary consideration.
> - Be understandable to a student who has never heard of ABTalks.
> - Handle real-world edge cases such as:
>   - First day with no streak
>   - A missed day
>   - An empty profile
> - Introduce at least one thoughtful idea that improves the student experience.
>
> **Out of Scope**
>
> You do not need to build:
> - Authentication
> - Real user accounts
> - A production database
>
> Use mocked data instead.
>
> A simple JSON file (written by you or generated using AI) is sufficient as long as the interface feels realistic.
>
> Also out of scope:
> - Recruiter dashboard
> - Admin panel
> - Matching ABTalks' current tech stack

*Defined the full three-screen scope (landing, dashboard, challenge day), the required edge cases, the mobile-first constraint, and what was explicitly out of scope.*

---

## 3. Prompt 3 — Request for code

> Give me the HTML code.

*Asked for the raw source of the three-screen mock app.*

---

## 4. Prompt 4 — Request for code (repeat)

> Give me the code which you have used to make this.

*Asked again for the underlying source code.*

---

## 5. Prompt 5 — "Make it feel real" enhancement brief

> **Make the App "Feel" Real (Functionality)**
>
> - **Add LocalStorage Persistence:** Right now, if a judge submits a task and refreshes the page, the state resets. Add a few lines of JavaScript to save the `PERSONAS` object to the browser's `localStorage`. When the page loads, check if `localStorage` has data and use that. This makes your mock app feel like a fully deployed, production-ready product.
> - **Simulate Authentication:** The persona switcher is brilliant for judging. To make it even better, add a "Sign in with GitHub" or "Sign in with Discord" button on the landing page that, when clicked, automatically logs the user in as the "brand new student" persona.
> - **Add a Confetti Animation on Submission:** When the user clicks "Submit today's proof," it currently just changes the screen. Hackathons are all about the user experience. Adding a lightweight confetti script (like `canvas-confetti`) when they submit a task gives a massive dopamine hit and will definitely make the judges smile.
>
> **2. Tie It Back to the ABTalks Brand**
>
> - **Integrate the Original Socials:** The original website footer emphasizes the ABTalks community with links to their Discord, Instagram, LinkedIn, and YouTube. You should add a "Community" tab or integrate these links into your user dashboard.
> - **Promote the Discord Review System:** Your text mentions, "Every task is reviewed by real students in Discord." Add a floating "Join Discord" button or an explicit CTA on the submitted task page where students can "Ask for review in Discord," linking directly to the ABTalks server.
>
> **3. Polish the UI/UX**
>
> - **Screen Transitions:** Currently, you swap screens by toggling the `hidden` class, which makes them snap instantly. You can add a simple CSS fade or slide-in animation.
>
>   ```css
>   .screen { animation: fadeIn 0.3s ease-in-out; }
>   @keyframes fadeIn { from { opacity: 0; transform: translateY(10px); } to { opacity: 1; transform: translateY(0); } }
>   ```
>
> - **Responsive Desktop Layout:** You've built a brilliant mobile-first app constrained to a 428px phone frame. While this is great for a mobile web app, judges often view projects on large monitors. Consider adding a CSS `@media` query that un-constrains the frame on desktops and turns the bottom nav into a persistent left-hand sidebar for a true "desktop dashboard" feel.
> - **A "Leaderboard" Screen:** Gamification is huge. You already track "Standing" (e.g., Top 12% this week). Adding a third navigation button at the bottom for a "Leaderboard" that shows mocked rankings of other students would make the 60-day challenge feel incredibly active and competitive.

*Requested three groups of upgrades: functionality (persistence, simulated auth, confetti), brand ties to ABTalks' real Discord/social presence, and UI polish (transitions, a desktop sidebar layout, and a leaderboard screen).*

---

## 6. Prompt 6 — Request for updated code

> Give me the raw HTML code for the above.

*Asked for the raw source of the updated app after the enhancement pass.*

---

## 7. Prompt 7 — This prompt log

> Create a PDF containing all the prompts used for this project.

*Requested this document (originally as a PDF, later converted to Markdown).*
