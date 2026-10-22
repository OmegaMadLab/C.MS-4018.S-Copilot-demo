# Session 1 – Create: from research to a leadership deck

**Catalogue items:** MS-4018.S03 (Word) + MS-4018.S02 (PowerPoint), with Researcher in the 90-minute version
**Story:** the leadership team of Contoso Ltd wants a **15-minute briefing next week** on *"AI skills for our workforce"*: where we stand, what the options are and what we should decide. A long research report already exists. Your job is to turn it into a 2-page brief and a deck you can present with confidence.

> **Why this story works everywhere:** every organisation in every country is facing the same question. It's also a natural bridge to "why are we in this training today".

## Demo assets

| File | Used in | Rule |
|------|---------|------|
| `AI_Skills_Research_Report.docx`: about 8 pages, looks like Researcher output | Acts 1–3 | 📖 READ-ONLY |
| `Contoso_Report_Template.docx`: branded Word template with placeholders | Act 2 | 🔁 **DUPLICATE** → rename the copy `AI_Skills_Executive_Brief_DEMO.docx` |
| `Contoso_Brand_Template.pptx`: Contoso theme, layouts and brand rules | Act 3 | 🔁 **DUPLICATE** → rename the copy `AI_Skills_Leadership_Deck_DEMO.pptx` |
| `Contoso_AI_Skills_Pulse_Survey_2026.docx`: internal survey | [90] Act 0 only | 📖 READ-ONLY |

## ✅ Before every delivery (10 min)

- [ ] Open `post-session/Teams_Chat_Messages_Sessions_1-3.html` in a browser tab, ready for the end of the session. If the customer has an AI policy link, paste it in the box at the top.
- [ ] Sign in as **Lynne Robbins** in an InPrivate or guest browser window, with no other accounts.
- [ ] 🔁 Duplicate `Contoso_Report_Template.docx` → `AI_Skills_Executive_Brief_DEMO.docx`.
- [ ] 🔁 Duplicate `Contoso_Brand_Template.pptx` → `AI_Skills_Leadership_Deck_DEMO.pptx`.
- [ ] Delete the `_DEMO` files from the previous delivery, so Copilot doesn't reference an old version.
- [ ] Open in browser tabs: `AI_Skills_Research_Report.docx`, `AI_Skills_Executive_Brief_DEMO.docx`, `AI_Skills_Leadership_Deck_DEMO.pptx`, Copilot Chat.
- [ ] Backup ready: `BACKUP_AI_Skills_Leadership_Deck.pptx` (see [setup step 4](../TRAINER-SETUP.md#4-generate-the-backups-20-min)).
- [ ] **[90]** The pinned conversation `DEMO – Researcher – AI skills` is less than a month old.

## Timeline

| 60-min version | 90-min version | Block |
|---|---|---|
| 00:00 – 00:12 | 00:00 – 00:18 | Welcome and [common intro](../README.md#common-introduction-all-sessions) (slides) |
| — | 00:18 – 00:28 | **[90] Act 0 – How the report was made (Researcher)** |
| 00:12 – 00:22 | 00:28 – 00:40 | Act 1 – Understand the report (Word, chat mode) |
| 00:22 – 00:35 | 00:40 – 00:55 | Act 2 – Write the brief (Word, edit mode, template) |
| 00:35 – 00:52 | 00:55 – 01:15 | Act 3 – Build the deck (PowerPoint) |
| 00:52 – 00:57 | 01:15 – 01:23 | Act 4 – Rehearse (speaker notes and quiz) |
| — | 01:23 – 01:27 | **[90] Bonus – Free-form deck and booking the meeting** |
| 00:57 – 01:00 | 01:27 – 01:30 | Wrap-up and Q&A |

---

## [90] Act 0 – How the report was made (Researcher)

🎬 **Say:** *"Last week the leadership team asked for a briefing on AI skills. Before writing anything, I asked Researcher to combine public studies with our internal survey. It takes a few minutes, so here's the prompt I used and the result."*
Open the pinned conversation **DEMO – Researcher – AI skills**. Walk through the prompt first, then scroll through the result.

**S1-R1 – Researcher prompt (already run, show it):**
```text
I need to brief our leadership team, in a 15-minute slot, on "AI skills for our workforce" and what we should do about it.
Use reliable public sources (for example the World Economic Forum Future of Jobs Report, the Microsoft Work Trend Index and OECD publications) together with my internal file /Contoso_AI_Skills_Pulse_Survey_2026, and:
1. Summarise the global trends on AI skills and adoption that matter for a company like ours, with figures.
2. Compare our internal survey results with the public benchmarks and show where we are behind.
3. Identify the functions where the gap is largest and the risk is highest.
4. Propose 3 strategic options with pros, cons, indicative cost and time to launch.
5. List the open questions for HR, IT and Legal.
Audience: executives, non-specialists. Format: structured report starting with an executive summary, tables where useful, and a source for every external fact. Clearly separate public facts, internal data and your own assumptions.
```

**S1-R1b – Answers to Researcher's clarifying questions (if asked):**
```text
Scope: all functions and countries. Time horizon: the next 12–24 months. Depth: executive level, about 6–8 pages. Language: English.
```

✅ **Expect:** a cited report with tables, separating public facts from internal data. Point out the citations and the clarifying questions Researcher asks before starting.
🎬 **Say:** *"I saved the result as a Word document. That's the report we'll work on now."* Switch to `AI_Skills_Research_Report.docx`.

**S1-R2 – Fact-check (run live in the same pinned conversation, about 1 minute):**
```text
Review the report you just produced. Create a table listing every number and date it contains, with these columns: Claim | Source | Type (public source / internal data / assumption) | Confidence (high/medium/low). Flag anything that is not directly supported by a source and tell me what I should verify before sharing it.
```
✅ **Expect:** a claims table. **Teaching point:** you are accountable for what you share, and Copilot helps you check.

---

## Act 1 – Understand the report (Word, chat mode)

🎬 **Say (60-min version):** *"A colleague sent me this 8-page report. I have to present to the leadership team next week, and I have 15 minutes and 2 pages. First, I want to understand it, without changing anything."*
🎬 **Say (90-min version):** *"Here's the report Researcher produced. Now let's turn it into something I can present."*

Open `AI_Skills_Research_Report.docx` → Copilot pane → **chat mode**.

**S1-P1 – Summary for my situation:**
```text
I have to brief our leadership team on this report in 15 minutes. Summarise it in 5 bullets: the key message, where Contoso stands compared with the benchmarks, the options, the recommendation, and the decision we need. Mention the section each point comes from.
```

**S1-P2 – Ask the document a real question:**
```text
Which two functions should we start with, and why? Use only the data in this report and quote the figures.
```

**S1-P3 – Plan before you write:**
```text
How would you turn this report into a 2-page executive brief for the leadership team? Propose a structure with section titles and the main content of each section, and tell me what you would leave out.
```

**S1-P4 – Teaching moment: chat doesn't edit:**
```text
OK, apply that structure and shorten this document to 2 pages.
```
✅ **Expect:** Copilot answers *in the chat* (or offers text to copy) and the document **doesn't change**.
🎬 **Say:** *"Chat mode is the safe mode. It reads, explains and proposes, but it never touches my file. To change a document, I switch to edit mode, and I'll do that in a copy, in our branded template."*

---

## Act 2 – Write the brief (Word, edit mode, template)

Open `AI_Skills_Executive_Brief_DEMO.docx` (your 🔁 copy of the template) → Copilot → **edit mode**.
🎬 **Say:** *"This is our corporate report template: styles, colours, table design. I want Copilot to write inside it and respect it."*

**S1-P5 – Draft the brief inside the template:**
```text
Using /AI_Skills_Research_Report, write an executive brief for the Contoso leadership team in this document, replacing the placeholder text.
Structure:
1. Executive summary (max 120 words)
2. Why now (3 global facts, with their source)
3. Where we stand (our survey results compared with the benchmarks)
4. Options compared (a table: option, cost year 1, time to launch, main risk)
5. Recommendation
6. Decisions we need from the leadership team
7. Next steps and owners (roles, not names)
Use the existing styles of this template for titles, headings, tables and the callout. Maximum 2 pages. Keep every figure exactly as it appears in the source report and do not add new figures.
```
✅ **Expect:** a 2-page brief written in the template styles (teal headings, branded table).
🛟 **If it's too long:** `Shorten the whole document to a maximum of 2 pages without removing the options table.`

**S1-P6 – Transform a section** (select the *Where we stand* section first):
```text
Turn this section into a table with the columns: Indicator | Contoso today | Public benchmark | Gap. Add one sentence below the table with the main takeaway.
```

**S1-P7 – Same content, different audience** (select the executive summary first):
```text
Rewrite this executive summary for our frontline managers in Customer Service and Operations: focus on what changes for their teams and what we will ask of them, plain language, no jargon, max 100 words.
```
🎬 **Say:** *"Same facts, different audience. This is one of the most valuable uses of Copilot in Word."* Then undo, or keep both versions.

**S1-P8 – Back to chat mode: check before sharing:**
```text
Compare this brief with /AI_Skills_Research_Report. Is any figure in the brief different from the source, or not present in it? Which statements are assumptions rather than facts? List them with the section where they appear.
```
✅ **Teaching point:** use **edit mode to change** and **chat mode to check**.

---

## Act 3 – Build the deck (PowerPoint)

Open `AI_Skills_Leadership_Deck_DEMO.pptx` (your 🔁 copy of the brand template) → Copilot.
🎬 **Say:** *"Our brand template is already open, so Copilot uses our theme, colours and layouts. I start from the brief I just wrote, not from a blank prompt."*

**S1-P9 – Create the deck from the brief:**
```text
Create a presentation for a 15-minute leadership briefing based on /AI_Skills_Executive_Brief_DEMO.
Storyline:
1. Title
2. The decision we need today
3. Why now (3 global facts)
4. Where we stand vs. the benchmarks
5. Where the gap is largest (by function)
6. Three options compared
7. Recommendation and KPIs
8. Next steps
Write each title as an action title that states the key message. Maximum 4 bullets per slide. Use the layouts of this template and do not add photos of people.
```
✅ **Expect:** about 8 slides in the Contoso theme. It can take 1–3 minutes, so talk over it about action titles.
🛟 **If it's slow or fails:** open `BACKUP_AI_Skills_Leadership_Deck.pptx` and continue from there.

**S1-P10 – Edit one slide, don't regenerate the deck** (go to the *Where the gap is largest* slide):
```text
Turn the content of this slide into a clustered bar chart comparing "Formal AI training %" and "Confident %" by function. Keep the action title and add one sentence of takeaway below the chart.
```
🎬 **Say:** *"Don't regenerate the whole deck for one change. Work slide by slide."*

**S1-P11 – Add a slide:**
```text
Add a new slide after slide 2 that answers "Why now?" in a single, powerful sentence, using a big-statement layout, with the key word highlighted.
```

**S1-P12 – Add an image** (on the *Recommendation* slide):
```text
Add an image to this slide that represents learning and growth in a modern workplace, with no people, in the colours of our template.
```

**S1-P13 – Edit the image** (select the image):
```text
Remove the background from this image.
```
Alternative: `Blur the background of this image so the text on the slide is easier to read.`
🛟 **If image editing isn't available in the tenant:** mention it and move on. Availability depends on the licence and the release.

**S1-P14 – Consistency pass:**
```text
Review all slide titles: make each one an action title of maximum 8 words, consistent in tone and tense. Do not change the slide content.
```

---

## Act 4 – Rehearse

**S1-P15 – Talk track in the speaker notes:**
```text
Write a talk track for presenting this deck in 15 minutes to our leadership team: for each slide give the time to spend, the key message and 2–3 talking points, and add them to the speaker notes of each slide.
```

**S1-P16 – Interactive sparring partner** (Copilot Chat, new conversation):
```text
Act as a sceptical CFO on our leadership team. Based on /AI_Skills_Leadership_Deck_DEMO, ask me the 5 toughest questions about this proposal, one at a time. Wait for my answer each time, then give me short feedback on how convincing it was and how to improve it.
```
🎬 Answer one or two questions live, ideally with an answer from the audience. **This is usually the wow moment of the session.**

---

## [90] Bonus – Free-form deck and booking the meeting

**S1-P17 – Free-form deck, different model** (Copilot Chat, select a different model, or a new blank presentation):
```text
Create a visually rich 6-slide internal presentation that explains why AI skills matter for Contoso and what we propose, based on /AI_Skills_Executive_Brief_DEMO. Use a modern, clean design with strong visual hierarchy, icons and charts. No photos of people. Internal use only.
```
🎬 **Say:** *"Brand template for official decks, free form for internal ideas. Notice how the model choice changes the result."*

**S1-P18 – Cliffhanger: book the meeting from chat** (Copilot Chat):
```text
Schedule a 30-minute meeting next week with Alex Wilber and Megan Bowen, at a time when all of us are available, preferably in the morning. Title: "AI skills for our workforce – decision". Add a short agenda with the 3 decisions we need and attach /AI_Skills_Leadership_Deck_DEMO.
```
🎬 **Say:** *"Booking meetings, preparing them and following up is exactly what Session 2 is about."*

---

## Wrap-up (3 min)

1. **Chat mode to understand and check, edit mode to change**, in a copy.
2. **Start from your own content and templates** (`/file`), not from a blank prompt.
3. **Edit slide by slide.** Don't regenerate the whole deck.
4. **You stay accountable:** fact-check figures and sources before sharing.

## After the session: share the take-away message

Open [Teams_Chat_Messages_Sessions_1-3.html](../post-session/Teams_Chat_Messages_Sessions_1-3.html) in a browser, click **Copy message** on *Session 1 – Create* and paste it into the meeting chat. The message contains the official guides, how to save, share and schedule prompts, and the reusable versions of today's prompts.

## Reusable prompt patterns (reference)

```text
Summarise this document for [audience] in [5] bullets: [key message], [our situation], [options], [recommendation], [decision needed]. Mention the section each point comes from.
```
```text
Using /[source document], write a [brief/report] for [audience] in this document with this structure: [sections]. Use the existing styles of this template. Maximum [2] pages. Keep every figure exactly as in the source.
```
```text
Rewrite this [section] for [audience]: focus on [what matters to them], plain language, max [100] words.
```
```text
Create a presentation for a [15]-minute [meeting] based on /[document]. Storyline: [slide list]. Action titles, max [4] bullets per slide, use the layouts of this template.
```
```text
Act as a sceptical [role]. Based on /[file], ask me the [5] toughest questions one at a time, wait for my answer, then give me feedback.
```
