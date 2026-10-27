---
name: questions
description: Suggest a short, varied list of good questions the user could ask next, based on exactly where the conversation has got to, to deepen understanding, test assumptions and open useful new directions. Use whenever the user types /questions, or asks what they should ask next, what questions to explore, what they might be missing, or "what would a good question be here?"
---

# Questions

## Why this exists

The quality of what you learn depends heavily on the quality of the questions you ask. Learners often ask only the next obvious question, or stop asking once an explanation sounds convincing. Good questions push past that: they probe why something is true, where it stops being true, how it connects to other things and how it would be used. This skill shows the user the questions worth asking at this point, and over time helps them learn to ask such questions themselves.

## Step 1: Read where the conversation is

Look at the conversation so far, paying most attention to the last few exchanges. Work out:

- the topic and the user's apparent goal (learning, deciding, building something, preparing for a conversation)
- what has already been explained or settled, so you don't suggest questions that have already been answered
- what has been glossed over, assumed or simplified
- where the user seemed uncertain, surprised or satisfied too quickly

If the user adds a focus after the command (e.g. "/questions about the evidence"), use it.

If the conversation has barely started, suggest questions that would help the user frame the topic well, rather than questions about content that hasn't been discussed.

## Step 2: Write the questions

Write 5–7 questions. Draw from a range of these types, choosing whichever are most valuable at this point; don't force every type in every time:

- **Mechanism**: why or how does this work? What causes it?
- **Boundaries**: when does this stop being true? What are the exceptions or edge cases?
- **Evidence**: how do we know? How strong is the evidence, and what would change the conclusion?
- **Assumptions**: what is being taken for granted? What if that assumption were wrong?
- **Connections**: how does this relate to something the user already knows, or to another idea in the conversation?
- **Contrast**: how is this different from a similar idea that is easily confused with it?
- **Application**: how would this be used in a real situation? What would doing it look like?
- **Alternatives**: what other views, approaches or explanations exist, and why might someone hold them?
- **Implications**: if this is true, what follows from it?

### What makes a good question here

- **Specific to this conversation.** "What are the limits of this?" is weak; "Does the predict-then-reveal effect still hold when learners already know the answer?" is strong. A question that could be pasted into any conversation is a sign of a generic one: rewrite it.
- **Not already answered.** Check each question against what has been said.
- **Worth the answer.** Prefer questions whose answers would change the user's understanding or decisions, over trivia.
- **Short and clear.** One question per item, no compound questions.
- **Written in the user's voice**, so they can ask it directly ("Why does…?", not "You could ask why…").

Order the list with the most valuable question first, and mark it as the suggested next question with a brief reason (one short sentence).

If a question can't be answered reliably without current information, research or the user's own context, add a short note to say so.

## Step 3: Present them

**If the inline widget tool (Visualizer / `show_widget`) is available**, show the questions as a compact list of clickable buttons, one per question, each labelled by type in small text. Clicking a question calls `sendPrompt()` with that question, so the user can ask it in one tap. Highlight the suggested next question. Follow the Visualizer's design guidance; load it first if you haven't in this conversation.

**Otherwise**, present a numbered list and tell the user they can reply with a number to ask that question.

Keep surrounding text minimal: one line before the list, and nothing after it except the prompt below.

## Step 4: Build the user's own questioning

The long-term goal is for the user to generate good questions themselves. After the list, add one short line inviting them to write their own question instead, if one of these prompted a better idea.

Occasionally (not every time), especially if the user has used the skill several times in a conversation, point out briefly which type of question they tend not to ask (e.g. "You often ask about application but rarely about evidence"), so they can notice the pattern.

## Answering a chosen question

When the user picks a question, answer it as a normal turn of the conversation. Don't automatically generate another list afterwards; the user can run /questions again when they want one.

## Language

Use the language the user is using. If they are learning a language and writing in it, write the questions in that language, at a level they can follow.
