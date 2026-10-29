---
name: worked-examples
description: Run case-based practice sessions in which the user works through sets of realistic, messy cases (real or synthetic) to build judgement, see what stays consistent and what varies across situations, and track which parts of their judgement need refinement over time. Use whenever the user types /case-studies, or asks for case studies, scenarios, worked cases, decision exercises or "situations to practise on" in any domain, or wants to add to or revisit their case library.
---

# Worked Examples

## Why this exists

Expertise in most real domains is less about knowing rules and more about recognising situations: which cues matter, when a familiar pattern applies, and when a case that looks similar actually calls for something different. That kind of judgement comes from experiencing many varied cases and comparing them. This skill gives the user that experience deliberately, and keeps a record of how their judgement develops.

The ideas behind it come from Cognitive Flexibility Theory (learning in ill-structured domains through many varied cases, viewed from several perspectives), the case method, and research on worked examples and on comparing contrasting cases.

## Core principles

- **Never a single case.** Always work in sets of at least two cases that are meant to be compared. Variance is only visible across cases.
- **The user decides first.** Every case asks the user to commit to a judgement before anything is revealed.
- **Cases are messy.** Real situations are ambiguous, and the skill is useless if every case has an obvious answer (see "Making cases messy").
- **Be honest about sources.** Always say whether a case is real or synthetic.
- **Track judgement, not just answers.** The goal over time is to find which parts of the user's judgement need refinement: cues they miss, patterns they over-apply, considerations they neglect.

## Step 1: Set up the session

Work out the domain and focus from the user's request and the conversation. If the domain is clear but the focus is broad, choose a concept or decision type that suits the user's level, and say what you chose.

**Check for a case library.** If the conversation or project knowledge contains the user's case library (see "The case library"), or the user gives a link to one, read it first. Use its judgement profile to target known weak spots, and avoid repeating cases already in it. If there is no library, carry on without one; saving is optional.

**Judge the user's level** from the conversation, the library and their answers so far. Re-assess as the session goes on and change format if needed. Don't ask the user to rate themselves unless you genuinely can't tell.

## Step 2: Choose the format

- **Newer to the domain**: start with a *worked case* that shows an expert's reasoning step by step, then a *partly worked* case where the user completes the reasoning, then one they do alone. Worked examples help beginners, but the benefit fades as competence grows, so move on quickly once they're coping.
- **Some experience**: *decision-point cases*. Present the situation up to the moment of decision; the user decides and explains why; then reveal what happened (or, for synthetic cases, what an expert would likely do) with analysis.
- **More advanced**: *expert-comparison cases*. At each stage of the case, ask what the user notices, what they expect to happen next and what they would do; then compare with expert reasoning. The point is to expose what experts see that the user doesn't.

## Step 3: Choose how the cases relate

Pick one structure per set:

- **Contrasting pair**: two cases that look nearly identical but call for different judgements. The debrief centres on the cue that distinguishes them.
- **Hidden match**: two or three cases that look very different on the surface but share the same underlying pattern.
- **Criss-cross**: the same concept seen across three or four varied cases, showing how it applies differently in each. Or one rich case viewed through several concepts.

Present the cases in a set together, or in quick succession, so they can be compared directly.

## Step 4: Source the cases

**Real cases** (found by web search or well-established from your knowledge) are preferred where they exist: business decisions, engineering failures and post-mortems, clinical case reports, legal judgments, historical events. When using them:

- Retell in your own words and cite sources. Don't reproduce substantial text from any source.
- Check that the key facts are supported by the sources. If a detail is uncertain, say so or leave it out; never fill gaps with invented specifics presented as fact.
- Real outcomes may be well known. If the user might recognise the case, consider describing it without identifying names until the reveal, and say you've done so.

**Synthetic cases** are fine, and in some domains (language use, interpersonal situations, many coding and teaching scenarios) they will be the main source. When using them:

- Label them clearly as synthetic.
- Base them on situations that genuinely occur, not on contrived puzzles.
- Remember that the "expert answer" for a synthetic case is your judgement, not a recorded outcome. Present it as reasoning to compare against, acknowledge where reasonable experts might differ, and don't overstate certainty.

A mixed set is fine: for instance, a real case with a synthetic variation built around it to create the contrast.

## Making cases messy

Before presenting a set, check each case against this list. Real situations usually have most of these:

- information that is incomplete, ambiguous or partly wrong
- irrelevant details mixed in with relevant ones, with nothing to signal which is which
- competing goals or constraints, so that any choice has costs
- more than one defensible option
- time pressure, limited resources or people with different interests
- an outcome influenced by luck as well as by the quality of the decision

If a case reads like a textbook example with one clean answer, rewrite it. Avoid giving away the answer through the framing, the order of information or a conspicuously emphasised detail.

## Step 5: Run the case set

Present one set at a time. For each case, ask a clear question that requires a committed judgement and a reason (e.g. "What would you do, and what in the situation makes you think so?"). Wait for the user's answers before revealing anything.

Keep the case text tight but complete: enough texture to be realistic, not so much that it becomes a reading exercise.

## Step 6: Debrief

For each set:

- Reveal what happened, or the expert reasoning for synthetic cases.
- Compare the user's judgement with it specifically: which cues they used well, which they missed, which they weighted wrongly.
- Draw out the comparison across the set: what stayed consistent, what varied, and which cue made the difference. Ask the user to state the distinction in their own words before you state it.
- Ask a counterfactual question where useful: "What would have to change in case A for your answer to case B to be right?"
- Be honest. Don't call a weak judgement good. Credit genuinely good reasoning even when the outcome went badly, and point out lucky outcomes from poor reasoning; the quality of the decision and the outcome are not the same thing.

Then offer another set, ideally targeting what this one revealed.

## The case library

Saving is optional. The skill must work fully without it.

At the end of a session, or when the user asks, offer once to save the session to their case library. If they decline or ignore it, don't ask again in that conversation.

**Where the library lives**: a single Claude Doc, created with the Claude Docs tools if they are available. If the user keeps the library in a Claude Project's knowledge, read it from there; if you can't update it directly, give the user the new entries to add, or update a linked Claude Doc copy if they have one. Without Docs tools, offer the entries as a Markdown file they can keep.

**Structure of the library**:

1. **Judgement profile** at the top, updated each time: strengths, recurring gaps (cues often missed, patterns over-applied, considerations neglected), and what's improved, with dates. Base this only on evidence from saved sessions; keep it short and specific. This is the most important part of the library.
2. **Tag index**: the list of concept tags used, so the user can ask for "every case involving X".
3. **Case entries**, newest first. Each entry contains:
   - title, date, domain and tags
   - source: real (with citations) or synthetic
   - the set it belonged to and how it relates to the other cases in the set
   - a short summary of the case
   - the user's judgement and reasoning, in brief
   - what happened or the expert reasoning
   - the key distinguishing cue or lesson, in a sentence

Keep entries concise: the library should be easy to scan.

**Revisiting**: when a library is available, you can offer to (a) create new cases that contrast with saved ones, (b) re-run a saved case with the outcome hidden, noting that the user may remember it, or (c) review the judgement profile and run a set aimed at a recurring gap.

## Language

Use the language the user is using. For language-learning domains, the cases themselves can be in the target language at a level the user can follow, with the debrief in the language they are most comfortable with.
