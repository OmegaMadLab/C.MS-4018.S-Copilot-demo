# One-time trainer setup (≤ 2 hours)

Do this **once per demo tenant**. After that, each delivery only needs the short *Before every delivery* checklist in the session README.

> **Assumptions:** you have a demo tenant with Microsoft 365 Copilot licences, the standard demo users (Lynne Robbins, Alex Wilber, Megan Bowen, Miriam Graham, Isaiah Langer) and their passwords. **Lynne Robbins is your presenter account** in every session and must have a Copilot licence. The other users don't need one.

| Step | What | Time | Sessions |
|------|------|------|----------|
| 1 | Upload the demo assets | 10 min | 1, 2, 3 |
| 2 | Seed the mailbox, chat and meeting | 60 min | 2 |
| 3 | Pre-run the agents and pin the results | 15 min (mostly waiting) | 1 [90], 3 [90] |
| 4 | Generate the backups | 20 min | 1, 3 |
| 5 | Verify that Copilot sees the content | 10 min | 2 |

---

## 1. Upload the demo assets (10 min)

Sign in as **Lynne Robbins**. In OneDrive, create this folder structure. You can use your own structure, but keep the file names unchanged because the prompts reference them.

```text
Copilot Demos/
├─ Session 1 - Create/
├─ Session 2 - Communicate/
└─ Session 3 - Analyse/
   └─ Analyst data/
```

| Upload from the repo | To OneDrive folder | Type |
|---|---|---|
| `session-1-create/demo-assets/word/AI_Skills_Research_Report.docx` | Session 1 - Create | 📖 READ-ONLY |
| `session-1-create/demo-assets/word/Contoso_Report_Template.docx` | Session 1 - Create | 🔁 master copy, duplicate before each delivery |
| `session-1-create/demo-assets/powerpoint/Contoso_Brand_Template.pptx` | Session 1 - Create | 🔁 master copy, duplicate before each delivery |
| `session-1-create/demo-assets/researcher/Contoso_AI_Skills_Pulse_Survey_2026.docx` | Session 1 - Create | 📖 READ-ONLY |
| `session-2-communicate/demo-assets/Project_Zava_Plan.docx` | Session 2 - Communicate | 📖 READ-ONLY |
| `session-3-analyse/demo-assets/excel/Sales_Q3_2026.xlsx` | Session 3 - Analyse | 🔁 master copy, duplicate before each delivery |
| `session-3-analyse/demo-assets/excel/Sales_Q2_2026.xlsx` | Session 3 - Analyse | 📖 READ-ONLY |
| `session-3-analyse/demo-assets/excel/Product_Descriptions_Review.xlsx` | Session 3 - Analyse | 🔁 master copy, duplicate before each delivery |
| `session-3-analyse/demo-assets/analyst/Service_Level_2026-0*.csv` (4 files) | Session 3 - Analyse/Analyst data | 📖 READ-ONLY |

- [ ] If the tenant asks for a sensitivity label, choose one **without protection** (*Public* / *General*). See [Pack rules](README.md#️-sensitivity-labels-and-other-tenants).
- [ ] Wait about 15 minutes before testing prompts that reference files with `/`. New files need time to be indexed.

## 2. Seed Session 2 (60 min)

Follow [session-2-communicate/seeding/SEEDING-KIT.md](session-2-communicate/seeding/SEEDING-KIT.md). It covers 3 emails, 2 low-priority emails, 6 chat messages and a recorded meeting you record **on your own** (no second person or device needed).

## 3. Pre-run the agents and pin the results (15 min, mostly waiting) – 90-minute versions only

Agents take several minutes to run, so never make the audience wait. Run each prompt once, **pin the conversation** in Copilot Chat (*… > Pin*), and open it during the session. Re-run if the result is older than about a month or if the agent has changed significantly.

- [ ] **Researcher:** Copilot Chat > Researcher > paste the prompt **S1-R1** from the [Session 1 plan](session-1-create/README.md#90-act-0--how-the-report-was-made-researcher). Answer its clarifying questions with **S1-R1b**. Rename the conversation to `DEMO – Researcher – AI skills`, then pin it.
- [ ] **Analyst:** Copilot Chat > Analyst > attach the 4 CSV files > paste **S3-A2** (the *precise* prompt) from the [Session 3 plan](session-3-analyse/README.md). Rename the conversation to `DEMO – Analyst – service levels`, then pin it.

## 4. Generate the backups (20 min)

The slowest live steps get a pre-generated backup in your own OneDrive. These backups aren't stored in the repo, so there's nothing to maintain.

- [ ] **Session 1 deck:** duplicate `Contoso_Brand_Template.pptx`, open the copy and run prompt **S1-P9** (create the deck from the brief). If you don't have a brief yet, use `/AI_Skills_Research_Report` instead of the brief. Save it as `BACKUP_AI_Skills_Leadership_Deck.pptx`.
- [ ] **Session 3 dashboard:** duplicate `Sales_Q3_2026.xlsx`, run prompts **S3-P1 → S3-P9** once (this is also your dry run), and save the copy as `BACKUP_Sales_Q3_2026_Dashboard.xlsx`.

## 5. Verify that Copilot sees the Session 2 content (10 min)

Signed in as Lynne, in Copilot Chat (Work mode), run:

```text
What do I have about Project Zava in my mail, Teams chats and meetings? List each item with its type and date.
```

- [ ] The result must list the email thread *Project Zava – Brazil go-live*, the chat *Project Zava core team* and the meeting *Project Zava weekly sync*. If something is missing, wait 30 minutes and try again. New content can take time to be indexed.

✅ **Setup complete.** From now on, use the *Before every delivery* checklist in each session README.
