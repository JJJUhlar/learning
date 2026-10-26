---
name: traffic-light
description: Map out all the areas of a topic and have the user rate their familiarity with each as red, amber or green, to decide where to focus their learning. Use whenever the user types /traffic-light, or asks to map out a topic, audit what they know, find their gaps, work out where to start, or plan what to learn next ("what don't I know about X?", "where should I focus?", "help me see the whole of this subject").
---

# Traffic light

## Why this exists

It is hard to know what you don't know. Learners tend to study what is in front of them, or what they already find comfortable, rather than what they most need. Laying out the whole territory of a topic and rating each part makes gaps visible and gives the learning a direction.

Self-ratings are useful but unreliable: people often rate things green because they recognise the name, not because they can use the idea. This skill treats the ratings as a starting point to be checked, not as the final word.

## Step 1: Pin down the scope

Use the topic the user names, or the topic of the conversation so far. If the topic is very broad (e.g. "machine learning", "French grammar") and the user's goal or level isn't clear from the conversation, ask one short question about what they are learning it for, then proceed. Don't ask if you can reasonably infer it.

## Step 2: Build the map

List the areas that make up the topic.

- Aim for roughly 12–25 items. Fewer leaves the map too coarse to be useful; more becomes tiring to rate.
- Group them into a few themed sections, and order them from foundational to advanced within each section.
- Include prerequisites the topic depends on, even if they belong to a neighbouring subject, and mark them as such.
- Give each item a short, concrete description of what it covers, so the user can judge their familiarity accurately. "Recursion" alone invites a quick guess; "Recursion: writing a function that calls itself, with a base case to stop it" makes it clearer what green would actually mean.
- Make items roughly similar in size. Don't put one huge area next to one tiny detail.
- Include only areas you are confident genuinely belong to the topic. Don't pad the list.

## Step 3: Collect the ratings

Define the levels clearly every time, because vague levels produce meaningless ratings:

- **Red (1)**: I haven't met this, or I couldn't explain what it is.
- **Amber (2)**: I recognise it and could explain some of it, but I'm shaky or would need to look things up.
- **Green (3)**: I could explain this to someone else and use it without help.

**If the inline widget tool (Visualizer / `show_widget`) is available**, build the map as an inline widget: each item shown with its description and three buttons for red, amber and green, grouped by section. Show a running count of each colour. End with a button that uses `sendPrompt()` to send all the ratings back into the chat, as item names and colours. Follow the Visualizer's design guidance, including making the colours readable in light and dark mode and not relying on colour alone (label the buttons too). Don't send until every item has a rating; show a short inline message saying which are missing.

**Otherwise**, present the map as a numbered list in plain text and ask the user to reply with numbers and ratings, e.g. "1:3, 2:2, 3:1…". Accept any reasonable format.

## Step 4: Spot-check the greens

Before drawing conclusions, check a few of the items the user rated green, particularly the foundational ones that other areas depend on. Ask one quick, concrete question at a time that someone who genuinely knew the area could answer easily, and that someone who only recognised it could not. Two or three checks are usually enough.

If a check reveals a gap, say so plainly and kindly, and move the item to amber. Explain that this is common and is exactly why the check exists. The user can skip this step if they choose.

## Step 5: Recommend where to focus

Give a short summary:

- the overall picture in a sentence or two (e.g. "solid foundations, gaps in the applied areas")
- the recommended starting point and why

When choosing what to focus on, consider dependencies first: a red or amber item that many others build on comes before anything that depends on it. After that, prioritise what matters most for the user's stated goal. Ambers are often quicker wins than reds, so mention any that would be worth consolidating early.

Recommend a short sequence (three to five items), not a plan for the whole map. Then offer a concrete way to begin on the first item, e.g. a problem to try, a guided questioning session, or an interactive demo.

## Coming back later

Suggest the user re-runs the traffic light after some study. If an earlier rating exists in the conversation, show which items have moved, so they can see their progress.

## Language

Use the language the user is using. For a language-learning topic, describe each item in the language the user is most comfortable reading, with examples in the target language where helpful.
