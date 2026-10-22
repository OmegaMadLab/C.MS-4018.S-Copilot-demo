# Session 2 – Communicate: Copilot as your personal assistant

**Catalogue items:** MS-4018.S04 (Outlook) + MS-4018.S06 (Teams)
**Story:** a day in the life of **Lynne Robbins, Project Lead of Project Zava**, the roll-out of a new customer-service platform at Contoso. The **Brazil go-live is at risk**: data quality issues, training clashing with the seasonal peak, and a knowledge base not yet translated. The sponsor, **Alex Wilber**, wants a status update by Thursday. Lynne missed yesterday's weekly sync. A new Training Lead, **Isaiah Langer**, joins next week.

> **Why this story works everywhere:** everyone has an overloaded inbox, missed meetings and a boss asking for a status update. Tell the audience to *"replace Project Zava with your own project"*.

## Demo assets and seeded content

| Item | Where | Rule |
|------|-------|------|
| `Project_Zava_Plan.docx` | Lynne's OneDrive | 📖 READ-ONLY |
| Email thread *Project Zava – Brazil go-live* plus 2 low-priority emails | Lynne's mailbox | Created once with the [seeding kit](seeding/SEEDING-KIT.md) |
| Teams group chat *Project Zava core team* | Lynne's Teams | Created once with the [seeding kit](seeding/SEEDING-KIT.md) |
| Meeting *Project Zava weekly sync* (recorded, Lynne didn't attend) | Lynne's calendar and Teams | Created once with the [seeding kit](seeding/SEEDING-KIT.md) |

> 🔁 **Nothing to duplicate in this session.** But **emails you send live** (S2-P5) and **meetings you book live** (S2-P11, S2-P13, S2-P14) are real. Delete them after the session so the next delivery starts clean, and so Copilot doesn't summarise last week's demo instead of the seeded content.

## ✅ Before every delivery (10 min)

- [ ] Open `post-session/Teams_Chat_Messages_Sessions_1-3.html` in a browser tab, ready for the end of the session. If the customer has an AI policy link, paste it in the box at the top.
- [ ] Sign in as **Lynne Robbins** (InPrivate or guest window), using the **new Outlook** or Outlook on the web.
- [ ] Delete the items created in the previous delivery: the sent status email (Sent Items), the meetings booked from chat, the 1:1 with Isaiah, focus-time blocks, and any scheduled prompts.
- [ ] Mark the 3 *Project Zava* emails and the 2 low-priority emails as **unread**.
- [ ] Open in tabs: Outlook (Inbox), Teams (Chat), Microsoft 365 Copilot Chat (**Work** mode).
- [ ] Check that the recap of *Project Zava weekly sync* opens.
- [ ] **[90]** If you show Notebooks: the notebook *Project Zava* exists (it takes 2 minutes to create, see Act 5).
- [ ] *Optional:* if the training meeting is transcribed and policy allows it, keep Teams open to show Copilot **in this meeting** (Act 3).

## Timeline

| 60-min version | 90-min version | Block |
|---|---|---|
| 00:00 – 00:12 | 00:00 – 00:18 | Welcome and [common intro](../README.md#common-introduction-all-sessions) |
| 00:12 – 00:25 | 00:18 – 00:34 | Act 1 – 08:30 Inbox under control (Outlook) |
| 00:25 – 00:35 | 00:34 – 00:46 | Act 2 – 10:00 Where are we really? (Copilot Chat across sources) |
| 00:35 – 00:48 | 00:46 – 01:02 | Act 3 – 11:30 The meeting I missed (Teams) |
| 00:48 – 00:56 | 01:02 – 01:14 | Act 4 – 14:00 Plan the week (Calendar) |
| — | 01:14 – 01:26 | **[90] Act 5 – 17:00 Let Copilot work for me (scheduled prompts, Notebook)** |
| 00:56 – 01:00 | 01:26 – 01:30 | Wrap-up and Q&A |

---

## Act 1 – 08:30 Inbox under control (Outlook)

🎬 **Say:** *"It's Monday morning. I'm Lynne, I run Project Zava, and my inbox is full. First, I teach Copilot what matters to me."*

**S2-P1 – Prioritize my inbox** (new Outlook: *Settings > Copilot > Prioritize my inbox*, or the *Prioritize* option in the inbox; paste these as your instructions):
```text
High priority: emails from Alex Wilber; anything about Project Zava that asks me for a decision, approval or input; any email with a deadline in the next 5 working days; escalations from country leads.
Low priority: newsletters, automated notifications, and FYI emails where I am only in CC.
```
✅ **Expect:** the Zava emails are flagged as high priority with a reason, and the newsletter and the Wi-Fi FYI as low priority. Prioritization can take a while to apply, so show the setting, explain it, and move on.
🎬 **Say:** *"These are instructions in plain language. No more rules with ten conditions."*

**Tour: the suggested prompts.** Open the thread *Project Zava – Brazil go-live* and show the ready-made Copilot suggestions at the top of the email (summary and suggested actions). *"You don't always need to write a prompt."*

**S2-P2 – Thread summary, chat mode** (Copilot pane, thread open):
```text
Summarise this thread in maximum 6 bullets: the decisions already taken, the open questions, and who is waiting for what from me, with the deadline if mentioned.
```
✅ **Expect:** Miriam's proposal (+2 weeks, two training groups), Megan's USD 18k approval by Wednesday, and Alex's status update by Thursday.
🎬 **Teaching point:** *"In the summary, Copilot can only answer in the chat. To write, I start a reply, and that's edit mode."*

**S2-P3 – Draft the reply, edit mode** (*Reply all* on Megan's email > *Draft with Copilot*):
```text
Reply to Megan and Miriam: approve the USD 18,000 extra effort for the data cleansing; confirm I support moving the Brazil go-live by two weeks, subject to steering committee approval; ask Megan to confirm by Wednesday whether the duplicates add a third week; thank Miriam for raising the risk early. Tone: friendly and concise, maximum 120 words.
```
Then refine with the buttons (*Make it more formal*, *Make it shorter*) or type:
```text
Make it more assertive and add a clear next step with a date.
```

**Email coaching:** on the draft, select **Coaching by Copilot** and show the feedback on tone, clarity and reader sentiment. *Don't send it,* discard it.

> 💬 **If asked about classic Outlook:** Copilot in classic Outlook covers summary, draft and coaching. Some newer features, such as Prioritize and some calendar capabilities, arrive in the new Outlook first.

---

## Act 2 – 10:00 Where are we really? (Copilot Chat across sources)

🎬 **Say:** *"Alex wants a status update. The information is spread across an email thread, a Teams chat and a meeting I missed. One prompt, three sources."*

Microsoft 365 Copilot Chat, **Work** mode. Type `/` to insert each reference:

**S2-P4 – Status across sources:**
```text
Give me the current status of Project Zava based on /Project Zava – Brazil go-live (email thread), /Project Zava core team (Teams chat) and /Project Zava weekly sync (meeting).
Structure:
1. Overall status (green / amber / red) with a one-sentence reason
2. Progress by workstream: IT and data migration, Brazil deployment and training, knowledge base
3. Top 3 risks with their impact on the go-live date
4. Decisions needed from the steering committee
5. Who owes what, by when
Cite the source (email, chat or meeting) for every point, and tell me if the sources contradict each other.
```
✅ **Expect:** status AMBER, the 3 risks (data quality, training vs. peak, Portuguese knowledge base) and the **contradiction**: 2 weeks in the email vs. "maybe 3" in the chat and meeting. Point to the citations.
🛟 **If a source isn't found:** run it again without that `/` reference, then explain that new content needs time to be indexed.

**S2-P5 – Draft and send from chat:**
```text
Draft an email to Alex Wilber with this status update, maximum 200 words, with the decisions needed in bold, the impact on customer satisfaction, and a clear recommendation at the end. Put Megan Bowen and Miriam Graham in CC. Subject: "Project Zava – status and decisions needed".
```
Review the draft, then ask Copilot to send it, or open it in Outlook and send it from there.
🎬 **Say:** *"I review before I send. Copilot drafts, I decide."* (Remember to delete it after the session.)

---

## Act 3 – 11:30 The meeting I missed (Teams)

Teams > Calendar or Chat > **Project Zava weekly sync** > **Recap**.
🎬 **Say:** *"I was invited to yesterday's sync but I couldn't join. In the past I'd have asked someone, or watched the recording. Now I just ask Copilot."*

Show the **default AI recap** first: notes, follow-up tasks, mentions and chapters.

**S2-P6 – Custom recap template** (recap > *Notes* > *Template* > *Custom*, or ask Copilot in the recap):
```text
Recap this meeting using this structure:
1. Decisions taken (with owner)
2. Actions (owner and due date, as a table)
3. What the attendees need from me (Lynne)
4. Risks and issues raised
5. Open questions
Maximum 250 words, bullet points, no small talk, use the names of the participants.
```

**S2-P7 – What did I miss:**
```text
I was invited to this meeting but could not attend. What did Alex and Megan decide about the Brazil go-live date, which concerns did they raise, and what is still unresolved? Quote the relevant moments of the transcript.
```

**S2-P8 – My calls to action:**
```text
What do the attendees expect from me after this meeting? List every action assigned to me, with the due date and the moment in the transcript where it was said.
```
✅ **Expect:** status update to Alex by Thursday, approve USD 18k by Wednesday, onboarding with Isaiah, update the RAID log, and put the knowledge base on the steering agenda.

**S2-P9 – Catch up on the group chat** (open the chat *Project Zava core team* > Copilot):
```text
Catch me up on this chat: what changed since the last email thread, and which messages are waiting for my answer?
```

**Optional (live): Copilot in this training meeting.** Only if the training meeting is transcribed and policy allows it. Open Copilot in the meeting:
```text
I joined late. Summarise what has been covered so far in this meeting in 5 bullets, with the time each topic started.
```
> 💬 **Facilitator:** if asked, explain it in one sentence: *"an agent that manages the agenda, timers and notes during a Teams meeting"*. We don't demo it because it depends on licensing and tenant settings.

---

## Act 4 – 14:00 Plan the week (Calendar)

🎬 **Say:** *"I have commitments now: a status update, an onboarding and a steering meeting to prepare. Let Copilot find the time."*

**S2-P10 – Find preparation time** (Copilot Chat, or Copilot in Outlook Calendar):
```text
Find me a 1-hour slot before Thursday to prepare the Project Zava status update, avoiding my existing meetings, and block it in my calendar as focus time.
```
🎬 **Say:** *"Copilot looks at my calendar. This is usually the wow moment."*

**S2-P11 – Onboarding 1:1 with the new team member:**
```text
Set up a 45-minute one-to-one next week with Isaiah Langer to onboard him to Project Zava, at a time when we are both free. Add a short agenda: project goal, timeline and milestones, his role in the training workstream, the current risks. Attach /Project_Zava_Plan.
```
🛟 **If booking from chat doesn't complete:** ask again (*"Yes, book the first slot"*) or open Outlook Calendar > *New event* > *Draft with Copilot*. Both paths are valid, so show the one that works in your tenant.

**[90] S2-P12 – Talk track for the steering meeting:**
```text
Write a talk track for a 15-minute steering meeting on Project Zava, based on the status update I sent to Alex: a 1-minute opening, the decisions needed with the options and my recommendation, the main risks, and a closing ask. Give the time for each part and 3 likely questions from Alex, with short answers.
```

**[90] S2-P13 – Book the steering meeting from chat:**
```text
Schedule a 30-minute meeting next week with Alex Wilber, Megan Bowen and Miriam Graham, at a time when all of them are available, preferably in the morning. Title: "Project Zava – Brazil go-live decision". Add an agenda with the decisions needed and attach /Project_Zava_Plan.
```

---

## [90] Act 5 – 17:00 Let Copilot work for me

🎬 **Say:** *"Everything I did today, I can ask Copilot to do every day, without remembering to ask."*

**S2-P14 – Scheduled prompt: Monday catch-up** (Copilot Chat > run the prompt, then *… > Schedule this prompt* > every Monday at 08:00):
```text
Look at my inbox, calendar and Teams chats from the last 72 hours and at this week's meetings. Tell me:
1. The 3 things I should start with today, and why
2. The meetings I need to prepare for, and what to read first for each
3. Messages waiting for my reply for more than 2 working days
Keep it under 150 words.
```

**S2-P15 – Scheduled prompt with an action: colour my calendar** (only if the tenant lets Copilot update calendar categories; show it, then delete the schedule):
```text
Look at my calendar for the next 7 days and assign these categories: "Project Zava" for meetings with Zava in the title, "1:1" for meetings with only one other person, and "Focus" for blocks without other attendees. Tell me what you changed.
```
🎬 **Say:** *"A scheduled prompt isn't only a reminder. It can act. Every Monday my calendar is colour-coded before I open it."*

**Optional – Copilot Notebook** (create the notebook *Project Zava* before the session; add `Project_Zava_Plan.docx` and the meeting as references):
```text
What has changed in the scope, timeline and budget since the project plan was written? List each change with the source and its impact on the Brazil go-live.
```
```text
Create a one-page onboarding brief for Isaiah Langer, who joins Project Zava next week as Training Lead: project goal, timeline and milestones, key people by role, current risks and decisions, how the team works, and where to find the main documents.
```

---

## Wrap-up (4 min)

1. **Tell Copilot what matters** (Prioritize), then let it summarise and draft. **You review and send.**
2. **One prompt, many sources:** `/` references to mail, chats, meetings and files, with citations.
3. **Missed meetings aren't lost:** recap, custom template, "what do they expect from me".
4. **Time is a resource Copilot can manage:** find time, book, prepare.
5. **[90] Automate with scheduled prompts.**

## After the session: share the take-away message

Open [Teams_Chat_Messages_Sessions_1-3.html](../post-session/Teams_Chat_Messages_Sessions_1-3.html) in a browser, click **Copy message** on *Session 2 – Communicate* and paste it into the meeting chat. The message contains the official guides, how to save, share and schedule prompts, and the reusable versions of today's prompts.

## Reusable prompt patterns (reference)

```text
High priority: emails from [people]; anything about [project/topic] that asks me for [a decision/approval/input]; emails with a deadline in the next [5] working days. Low priority: [newsletters, notifications, FYIs in CC].
```
```text
Summarise this thread in max [6] bullets: decisions taken, open questions, and who is waiting for what from me, with deadlines.
```
```text
Give me the current status of [project] based on /[email thread], /[Teams chat] and /[meeting]. Structure: overall status (RAG) with reason; progress by [workstreams]; top [3] risks; decisions needed; who owes what by when. Cite the source of every point and flag contradictions.
```
```text
I was invited to this meeting but could not attend. What did [people] decide about [topic], which concerns were raised, and what is unresolved? Quote the relevant moments.
```
```text
Find me a [1]-hour slot before [day] to prepare [task], avoiding my existing meetings, and block it as focus time.
```
```text
Look at my inbox, calendar and Teams chats from the last [24/72] hours. Tell me the [3] things to start with, the meetings to prepare for, and messages waiting for my reply for more than [2] days. Under [150] words.
```
