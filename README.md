# MS-4018 Copilot standard sessions – trainer pack

A ready-to-deliver pack for three short Microsoft 365 Copilot sessions, each available as a **60-minute** or a **90-minute** version. The pack is standard: a trainer who knows MS-4018 can deliver it after a one-time setup of **2 hours or less**, without customising it for each customer.

| # | Session | Catalogue items | Apps | 90-minute extra |
|---|---------|-----------------|------|-----------------|
| 1 | [Create – from research to a leadership deck](session-1-create/README.md) | MS-4018.S03 + MS-4018.S02 | Word, PowerPoint | Researcher agent |
| 2 | [Communicate – Copilot as your personal assistant](session-2-communicate/README.md) | MS-4018.S04 + MS-4018.S06 | Outlook, Teams, Copilot Chat | Scheduled prompts, meeting prep, Notebooks |
| 3 | [Analyse – from raw data to insight](session-3-analyse/README.md) | MS-4018.S05 | Excel | Analyst agent |

All three sessions use one fictitious company, **Contoso Ltd**: 8,500 employees in 12 countries, selling home and office products worldwide. Do not rename it for each customer. The stories work in every industry. Tell the audience to *"listen for the pattern, then think of your own files"*.

---

## How to use this pack

1. **Once per demo tenant:** follow [TRAINER-SETUP.md](TRAINER-SETUP.md). It takes about 2 hours for all three sessions, and most of that is the Session 2 seeding.
2. **Before each delivery:** complete the *Before every delivery* checklist at the top of the session README (10–15 minutes).
3. **During the delivery:** keep the session README open on a second screen. Each demo has
   - 🎬 **Say:** one or two lines of story, so you remember *why* you are doing this step
   - 💬 **Prompt:** in a code block. Use the copy button at the top right of the block.
   - ✅ **Expect:** what a good result looks like
   - 🛟 **If it goes wrong:** a steering prompt or the backup to show

   Blocks marked **[90]** are for the 90-minute version only. Skip them in the 60-minute version.
4. **At the end of the session:** open [post-session/Teams_Chat_Messages_Sessions_1-3.html](post-session/Teams_Chat_Messages_Sessions_1-3.html) in a browser, click **Copy message** for your session and paste it into the meeting chat. It includes the official guides, how to save, share and schedule prompts, and the reusable prompts from the session. If the customer shared their AI policy link, paste it in the optional box at the top first.
   > GitHub shows HTML files as source code. Download the file, or open it from your OneDrive, and then open it in a browser.

## Pack rules

### 📄 Duplicate first
Some demo files are **changed by Copilot during the demo** (Copilot writes into the Word template, fixes formulas in Excel, and so on). Never demo on the original:

- Each session checklist marks these files with **🔁 DUPLICATE**.
- Before each delivery, copy the file in OneDrive (*… > Make a copy*) and rename the copy with the suffix `_DEMO`, for example `Sales_Q3_2026_DEMO.xlsx`.
- Demo on the `_DEMO` copy. After the session, delete it.
- Files marked **📖 READ-ONLY** are only read by Copilot, so you don't need to duplicate them.

### 🏷️ Sensitivity labels and other tenants
The demo assets in this repo have **no encryption, no rights restriction (IRM) and no password**. They can be uploaded to any demo tenant and Copilot can read them there.

- **Never apply a label that encrypts the file**, for example *Confidential* or *Highly Confidential* with protection. Encrypted files can't be opened by Copilot in another tenant.
- Your demo tenant may require a label on upload. If so, pick a label with **no protection**, such as *Public* or *General*.
- **Files created or edited in a corporate tenant can pick up that tenant's default label, and some default labels encrypt.** Before you commit an Office file, open it in desktop Office and check *Sensitivity* on the ribbon. If the label encrypts the file, change it to *Public* or *General* (no protection), save, then commit. *File > Info* must show no *Protect* or *Restrict Access* banner.
- Markdown and CSV files can't carry a label and need no check.

### 🧑‍🤝‍🧑 People
Session 2 uses the standard Microsoft 365 demo-tenant users: Lynne Robbins, Alex Wilber, Megan Bowen, Miriam Graham and Isaiah Langer. If your tenant uses different names, change them **only** in the seeding kit and in the Session 2 prompts.

### 🎯 Show the pattern, not the product tour
Customers already know "summarise this". The prompts in this pack are **contextual and structured** (role, goal, sources, format, constraints). Point this out every time you paste one.

---

## Common introduction (all sessions)

Slides cover the course agenda and the introduction. Then move to the whiteboard and the demos. Use about **12 minutes in the 60-minute version** and **15–20 minutes in the 90-minute version**.

1. How Microsoft 365 Copilot works: LLM + **Work IQ** (your mail, files, meetings, chats, people) + the apps, with **permissions respected**
2. Choosing a model (Auto, quick response, deeper reasoning)
3. Prompt basics: **Goal – Context – Source – Expectations**, then iterate
4. Copilot Chat vs. Copilot in the apps; **chat mode vs. edit mode** in the apps
5. What an agent is, in one sentence. Researcher and Analyst are introduced only in the 90-minute versions.
6. Responsible use: verify, cite sources, follow your organisation's AI policy

---

## Repo structure

```
MS-4018-Copilot-Standard-Sessions/
├─ README.md                ← this file: rules and common intro
├─ TRAINER-SETUP.md         ← one-time setup, about 2 h, all sessions
├─ session-1-create/
│  ├─ README.md             ← delivery plan, 60/90 min, checklist and prompts
│  └─ demo-assets/
│     ├─ word/              ← AI_Skills_Research_Report.docx, Contoso_Report_Template.docx
│     ├─ powerpoint/        ← Contoso_Brand_Template.pptx
│     └─ researcher/        ← Contoso_AI_Skills_Pulse_Survey_2026.docx   [90]
├─ session-2-communicate/
│  ├─ README.md
│  ├─ seeding/SEEDING-KIT.md ← emails, chat, meeting role-play script
│  └─ demo-assets/          ← Project_Zava_Plan.docx
└─ session-3-analyse/
   ├─ README.md
   └─ demo-assets/
      ├─ excel/             ← Sales_Q3_2026.xlsx, Sales_Q2_2026.xlsx, Product_Descriptions_Review.xlsx
      └─ analyst/           ← Service_Level_2026-06…09.csv (same structure, 4 months)   [90]
└─ post-session/
   └─ Teams_Chat_Messages_Sessions_1-3.html ← end-of-session chat message per session (copy button)
```

**Asset count:** 3 files for Session 1, 1 for Session 2 (plus the seeding kit), and 3 for Session 3, plus 4 CSV files that share one structure. No backups are stored in the repo. The checklists tell you which results to pre-generate in your own tenant.

## Ownership and changes

Each session has **one owner**, who keeps the demos working and approves changes. Other trainers don't edit the files directly:

- **Something broke or could be better:** open an issue with the session, the prompt ID (for example `S3-P7`), what you expected and what happened.
- **You want to change a file:** open a pull request. The session owner reviews and merges it.

| Session | Owner | Reviewers |
|---------|-------|-----------|
| 1 – Create | [owner] | [reviewers] |
| 2 – Communicate | [owner] | [reviewers] |
| 3 – Analyse | [owner] | [reviewers] |

All companies, people and figures in the demo assets are fictitious. Public figures quoted in the Session 1 research report come from the publications listed in its *Sources* section. Check them again before you quote them as current.
