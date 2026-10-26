---
name: demo
description: Build a small interactive demo, inline in the chat, that helps the user understand one concept by predicting, experimenting and reporting back. Use whenever the user types /demo, or asks to see, explore, play with or visualise how something works, especially in maths, coding and science ("show me how this changes", "can I try it?", "visualise this algorithm"). Even when not asked, offer a demo in one line if a concept would clearly click better by experimenting with it, but don't build one unasked.
---

# Interactive demo

## Why this exists

Watching an animation or moving a slider feels like learning, but passive viewing and aimless fiddling teach surprisingly little. What works is committing to a prediction first, then testing it, then explaining the result. Every demo should be built around that cycle, not around looking impressive.

## Where it lives

Always build the demo as an inline widget in the chat (the Visualizer / `show_widget` tool), never as a separate published page or downloadable file. The user wants a seamless experience without leaving the conversation. Load the Visualizer's design guidance (`read_me`, usually the `interactive` module) before building, and follow it for styling, dark mode and layout.

If no inline widget tool is available, say so in one line and offer to walk through the same predict-then-test cycle in text instead.

## One concept per demo

Pick the single idea the demo should make click, and cut everything else. A good test: can you state, in one sentence, what the user should understand after using it? If the concept has several parts, build one demo, debrief it, and then offer the next.

Keep controls few. Every control the user can change should be one that matters for the concept; extra knobs invite aimless fiddling.

## Choose the interaction to fit the concept

Don't default to sliders. Choose whatever lets the user act on the idea most directly. For example:

- **Continuous parameters** (a coefficient, a rate, a mass): sliders or number inputs.
- **Geometry and graphs**: drag points, vectors or shapes directly on the diagram.
- **Algorithms and code execution**: step forwards and backwards through execution, showing the state (variables, the stack, an array being sorted) at each step. Let the user edit inputs or a small piece of code and re-run.
- **Discrete choices** (which data structure, which reaction condition, which rule applies): toggles, buttons or clickable options.
- **Ordering and classification**: arrange or sort items, or drop them into categories, then check.
- **Probability and randomness**: run trials one at a time and then many at once, so the user sees both the noise and the long-run pattern.
- **Systems over time** (populations, orbits, circuits): play, pause and step controls, with one or two variables the user can change.

The prediction can take different forms too: choosing from misconception-based options, typing a numeric estimate, clicking where something will land, sketching the expected curve, or predicting the next step of an algorithm before revealing it. Pick whatever fits the concept.

## The structure of every demo

1. **Predict.** Ask the user to commit to a prediction before the interactive part unlocks. If you use multiple-choice options, each wrong option should represent a specific, plausible misconception. Include a small, quiet "skip prediction" option, because the user may choose to skip and that's fine.
2. **Test.** Unlock the interactive part. Show linked representations where possible, so that changing one thing updates the others together: equation and graph, code and memory state, formula and simulation, numbers and picture.
3. **Respond to the prediction.** When the user reaches the case they predicted, compare it with what they chose. Don't explain the answer; ask a short question or point to what to look at ("Compare where each wave finishes its first cycle").
4. **Challenge.** Give two or three small goals that require working backwards from an outcome to an input ("Make exactly three waves fit", "Find an input where the loop never terminates"). Mark each as done automatically when achieved.
5. **Report back.** End with a button that uses `sendPrompt()` to send the user's prediction and challenge progress back into the chat, and asks Claude for one question to check their understanding. This closes the loop without the user typing anything.

## Correctness

A demo with a subtle bug teaches something false, convincingly. Before presenting:

- Check computed values against known cases and limits (e.g. b = 1 should give the original graph; zero friction should conserve energy; an empty list should sort to an empty list).
- Make sure challenge targets are actually reachable with the controls' ranges and step sizes.
- Round every displayed number sensibly.
- Simplify where needed, but say so in the chat if the model is a simplification ("this ignores air resistance").

## In the chat around the demo

Before the demo, write one or two sentences setting up the question; don't explain the concept, because that would give away the prediction. After the demo, say nothing more until the user reports back or replies.

When the user reports back, respond in the spirit of guided questioning: ask one question that checks whether they understand *why* the result happens, not just *what* happened. If they want, hand over to the quiz or Socratic skills.

## Language

Use the language the user is using in the conversation, including for the text inside the widget.
