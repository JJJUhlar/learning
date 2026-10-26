---
name: quiz
description: Create a challenging multiple-choice quiz on whatever the current conversation has been about, to expose gaps in the user's understanding and steer what they study next. Use whenever the user types /quiz, or asks to be quizzed, tested or checked on what they have been learning ("test me on this", "do I actually get this?", "give me some practice questions"), even if they don't say the word "quiz".
---

# Quiz

## Why this exists

Following an explanation in a chat feels like learning, but recognising an idea is not the same as being able to use it. This quiz checks whether understanding has actually transferred. It should be hard to pass by pattern-matching on wording from the conversation. A quiz the user aces without effort has failed at its job, because it has told them nothing.

## Step 1: Decide what to test

Look back over the conversation and list the ideas that were taught or discussed. Prioritise:

- core concepts that the rest of the topic depends on
- anything the user got wrong, hesitated over, or asked about more than once
- distinctions between ideas that are easily confused
- things that were explained to the user but that they never practised themselves

Ignore tangents. If the user names a focus after the command (e.g. "/quiz the subjunctive"), concentrate on that. If the conversation has no substantial topic yet, ask the user what they would like to be quizzed on rather than inventing one.

Stay within what the conversation covered. One "stretch" question that applies an idea to an unfamiliar case is fine; label it as a stretch question.

## Step 2: Write the questions

Default to 6 questions unless the user asks for a different number.

Weight the quiz towards questions that require understanding rather than memory:

- **Application**: use the idea on a new example that did not appear in the conversation.
- **Discrimination**: pick which of several similar cases fits the rule, or spot the error.
- **Prediction and explanation**: what would happen if…, why does…
- **Recall**: at most one or two, and only for facts that genuinely matter.

Do not reuse examples or phrasing from the conversation. New examples test understanding; reused ones test memory of the chat.

### Distractors

The wrong options are what make the quiz diagnostic, so put the most care into them.

- Each distractor should represent a specific, plausible misconception: ideally one the user showed in the conversation, otherwise one learners commonly hold. Keep a private note of which misconception each distractor stands for, so you can explain it in the debrief.
- Make all options similar in length, grammar and level of detail, and vary the position of the correct answer. Test-wise users can otherwise guess from surface features.
- No "all of the above", "none of the above" or joke options.
- There must be exactly one defensibly correct answer. For each question ask: could an expert argue for a second option? If so, rewrite it.
- Verify every correct answer before presenting. If you are not certain of a fact, do not build a question on it.

### Language

Write the quiz in the language the conversation has been in. For a language-learning topic, test the target language itself (sentences to complete, errors to spot, the right form to choose), not facts about the language.

## Step 3: Present the quiz

Open with one line asking the user to answer without scrolling back or looking anything up: the aim is to find gaps, not to get a good score.

**If the `quiz_display_v0` tool is available**, use it. Hints should nudge, not give the answer away. Each explanation should say why the correct answer is right and briefly why the most tempting distractor is wrong. Do not reveal answers in your chat text.

**Otherwise**, present the questions as numbered text with options A–D and withhold the answers. Ask the user to reply with their answers and, for each, whether they were *sure* or *guessing*.

Confidence matters: a confident wrong answer is the most valuable result a quiz can produce, because it reveals a misconception the user did not know they had. A lucky guess that happened to be right should not count as understanding.

## Step 4: Debrief

The quiz card may not report the user's answers back to you. If you used it, ask the user afterwards which questions they got wrong (and which correct ones were guesses) so you can debrief properly.

In the debrief:

- Give the score briefly. Do not inflate praise; acknowledge genuine strengths specifically.
- For each wrong answer, name the misconception that the chosen option represents and explain the correct idea concisely.
- Group the results into themes, e.g. "solid on X; Y is shaky, especially when Z".
- Recommend one or two concrete next steps. Usually this means giving the user a problem on the weak area to attempt *before* any further explanation, rather than re-explaining straight away.
- Offer a follow-up quiz aimed at the weak areas, using new questions on the same ideas rather than repeating the old ones.

If the user gets everything right and was sure each time, say so plainly, then offer a harder round (more transfer, multi-step reasoning), because the quiz was probably too easy to be informative.
