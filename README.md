# The Feedback Dilemma

A short, interactive branching scenario that lets a manager practise giving difficult feedback and see the consequences of each choice play out. Built on the Situation–Behaviour–Impact (SBI) model. Built by [The Human Co.](https://thehumanco.org)

This is one of a series of tools I build to show what scenario-based learning can do when it is built properly. It is a demonstration, free to use, no sign-up.

## What it does

- Plays a 6-minute workplace scenario (Alex has missed two deadlines) where you choose how to open, respond, and close
- Scores each choice and shows a final readout
- Teaches the SBI frame with a worked before/after example
- Generates a printable feedback cheat-sheet

## Tech

Single static file — everything (markup, styles, and the scenario logic) lives inline in `index.html`. No backend, no API: it all runs in the browser. Deployed as a static site on Vercel.

## Run locally

```bash
npx serve .
```

Then open the served URL.

## Provenance

Originally deployed to Vercel on 16 August 2025 via direct CLI upload, with no connected git repository. The source was recovered from the live deployment (`feedback-demo-omega.vercel.app`) and committed here on 12 June 2026 so it is version-controlled and editable again. The first commit is the faithful recovered original, exactly as it was live.

## Known issues (in the recovered original)

Documented at recovery so the fix history is clear:

1. **Choice feedback lands one screen late.** The intro choice increments the same step counter used to target the `#fb1/#fb2/#fb3` feedback divs, so each choice's explanation appears on the following screen — and the final choice's explanation writes to a non-existent `#fb4` and is lost.
2. **Score scale mismatch.** Four scored choices give a possible 8 points, but the result is shown out of 6 — a strong run can read `8 / 6`.
3. **Doubled denominator.** `finalize()` writes `"<score> / 6"` into a span that is already followed by `/ 6`, rendering `X / 6 / 6`.
4. **Minor.** `showScreen()` is defined twice (identical); harmless.

---

Part of The Human Co. — AI training and implementation for people-first organisations.
