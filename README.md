# The Feedback Dilemma

A free, interactive tool that lets a manager practise giving difficult feedback and see the consequences of each choice play out. It is built on the Situation, Behaviour, Impact (SBI) model. Made by [The Human Co.](https://thehumanco.org)

You play the manager. Alex, a normally reliable team member, has missed two deadlines. How you open the conversation changes how Alex responds, and the conversation genuinely branches from there. It is one of a series of tools built to show what scenario based learning can do when it is built properly. Free to use, no sign up.

## What it does

- A short branching scenario across four decisions: the opener, the response, the pivot, and the close.
- Real branching. Alex has a rapport state that your choices move. Open well and Alex tells you the real cause. Push too hard and Alex shuts down, and you have to repair it before you can get anywhere.
- It never telegraphs the right answer. Options are neutral and shuffled. The verdict and the reasoning only appear after you have committed.
- An end of run review of every decision: what you chose, the strongest move, and why, with the skill it trains.
- A shareable result link and a printable one page cheat sheet.

## Accessibility

Built to be usable by anyone. Every choice is a real keyboard operable button, focus moves to each new screen, an aria-live region announces feedback and state changes, nothing relies on colour alone, and it reflows cleanly on a phone. Audited with axe-core: zero WCAG 2.1 A/AA violations on the intro, decision, and result screens.

## Tech

One self contained `index.html`. Markup, styles, and a small data driven scenario engine (a `NODES` graph plus a `rapport` state variable) all live inline. No backend, no API, no external or runtime dependencies, no fonts loaded over the network. It works by opening the file, stays embeddable in an `<iframe>`, and can be downloaded as a single file. Deployed as a static site on Vercel.

## Run locally

```bash
npx serve .
```

Then open the served URL.

## Provenance

Originally deployed to Vercel in August 2025 via direct CLI upload, with no connected git repository. The source was recovered from the live deployment in June 2026, version controlled, and then rebuilt into the current branching, accessible version. The faithful recovered original is preserved in the git history (the first commit).

---

Part of The Human Co. AI training and implementation for people first organisations.
