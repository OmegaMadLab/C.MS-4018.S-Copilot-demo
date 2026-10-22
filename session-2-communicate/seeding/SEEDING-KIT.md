# Session 2 – Seeding kit (one-time, about 60 minutes)

This kit creates the Microsoft 365 content that Copilot reads during Session 2: an email thread, two low-priority emails, a Teams group chat and a recorded meeting with a transcript. **Lynne Robbins** is the presenter and receives everything.

| Role | Demo user | Copilot licence needed? |
|------|-----------|--------------------------|
| Project Lead (**presenter**) | Lynne Robbins | **Yes** |
| Executive Sponsor (VP Customer Operations) | Alex Wilber | No |
| IT & Data Migration Lead (organises the weekly sync) | Megan Bowen | No (needs Teams with transcription) |
| Country Lead Brazil | Miriam Graham | No |
| Training Lead (joins next week) | Isaiah Langer | No |

> **Tips**
> - Use one **InPrivate** or browser-profile window per user, so you don't have to sign in and out each time.
> - Each message is in a code block: copy it, paste it, send it.
> - The content uses **relative dates** ("by Thursday", "Month 5"), so the kit keeps working for future deliveries. Re-seed only if the content is more than about 3 months old, or if you want a fresh "last 7 days" story.
> - Send the emails **in the order shown**, a few minutes apart, as **Reply all** in the same thread.

---

## A. Email thread "Project Zava – Brazil go-live" (15 min)

### A1 – Miriam Graham → Lynne Robbins, CC Megan Bowen
**Subject:**
```text
Project Zava – Brazil go-live
```
**Body:**
```text
Hi Lynne,

I want to raise a risk early. The data migration rehearsal last weekend showed that about 8% of the historical cases (roughly 96,000 records) have a missing or invalid customer ID. Megan's team says cleaning them needs about two extra weeks.

On top of that, agent training for the 140 São Paulo agents is planned for the two weeks before go-live, which now overlaps with our seasonal peak. My supervisors are worried about pulling agents off the phones in that period.

My proposal: move the Brazil go-live by two weeks and run the training in two groups of 70 agents. Can you let me know by Friday if you support this, so I can brief the supervisors?

Thanks,
Miriam
```

### A2 – Megan Bowen → Reply all
```text
Hi both,

Confirming Miriam's numbers. We have a cleansing script ready and can confirm migration readiness by the end of next week if we start on Monday.

The implementation partner needs about USD 18,000 of extra effort for the cleansing. That is within Lynne's approval limit, but the go-live date change itself needs steering committee approval.

Lynne, can you approve the extra effort by Wednesday?

Megan
```

### A3 – Alex Wilber → Reply all
```text
Lynne,

I'm open to moving the date, but I don't want surprises on customer satisfaction during the peak. Before the steering committee, please send me a short status update with the options, the impact on CSAT and your recommendation, by Thursday.

Alex
```

## B. Two low-priority emails for the *Prioritize my inbox* demo (5 min)

### B1 – Isaiah Langer → Lynne Robbins
**Subject:**
```text
Contoso Learning newsletter – new courses this month
```
```text
Hi all,

This month's Contoso Learning newsletter: 12 new courses in the catalogue, including "Presenting with confidence" and "Excel essentials". Lunch-and-learn sessions are open for registration on the intranet.

Happy learning!
The Learning team
```

### B2 – Miriam Graham → Megan Bowen, **CC Lynne Robbins**
**Subject:**
```text
FYI – São Paulo office Wi-Fi maintenance on Saturday
```
```text
Hi Megan,

Just FYI: the São Paulo office Wi-Fi will be down for maintenance on Saturday morning. No action needed.

Miriam
```

---

## C. Teams group chat "Project Zava core team" (15 min)

1. As **Lynne**, create a new group chat with **Megan Bowen** and **Miriam Graham**. Name it:
```text
Project Zava core team
```
2. Post the messages in this order, each one as the user shown:

**C1 – Megan:**
```text
Rehearsal results are in: 1.2 million cases migrated in 31 hours, which is within the cut-over window. The issue is the ~96,000 cases with missing customer IDs. Details in the email thread.
```
**C2 – Miriam:**
```text
Supervisors in São Paulo are OK with training in two groups of 70, but not in the peak weeks. If the go-live moves by two weeks, training would fall outside the peak. 👍
```
**C3 – Megan:**
```text
Update: we also found duplicates in the customer table. If we have to fix those too, cleansing could take three weeks instead of two. I'll know by Wednesday.
```
**C4 – Miriam:**
```text
Another risk: only 60 of the 180 knowledge articles are translated into Portuguese so far. The agency says the rest will take four weeks.
```
**C5 – Megan:**
```text
Good news: the telephony integration test passed yesterday. ✅
```
**C6 – Megan:**
```text
@Lynne Robbins can you confirm the USD 18k for the partner by Wednesday? And who is onboarding Isaiah next week?
```

> **Why C3 matters:** the email says *two weeks*, the chat says *maybe three*. Copilot should flag this contradiction in prompt S2-P4.

---

## D. Meeting "Project Zava weekly sync", recorded by you alone (25 min)

You don't need other people or a second device. You read every part yourself, **saying the speaker's name before each line**. Copilot uses the names to attribute the content in the recap.

1. As **Megan Bowen**, schedule a Teams meeting now (or in 5 minutes):
   - **Title:**
     ```text
     Project Zava weekly sync
     ```
   - **Attendees:** Lynne Robbins, Miriam Graham, Alex Wilber
   - Leave the meeting options at their defaults. Recording and transcription must be allowed.
2. **Lynne doesn't join.** That's the story: "the meeting I missed".
3. As **Megan**, join, then **Start recording and transcription** (*More > Record and transcribe*).
4. Read the script below **out loud**, slowly, including the names. It takes about 4–5 minutes.
5. Stop the recording and leave the meeting. The recap and transcript appear for invitees after a few minutes, sometimes up to an hour.

### Script (read everything, including the speaker names)
```text
MEGAN: Megan here. Welcome to the Project Zava weekly sync. Lynne can't join today, so I'm chairing. We have three topics: the data migration, the Brazil go-live date and training, and the knowledge base.

MEGAN: Megan again, on the data migration. The rehearsal migrated 1.2 million cases in 31 hours, so the cut-over window is fine. But around 96,000 cases, about 8 percent, have a missing customer ID, and we found duplicates in the customer table. Cleansing needs two weeks, possibly three if we also fix the duplicates. I'll confirm by Wednesday.

MIRIAM: This is Miriam. From the Brazil side, I'd rather move the go-live by two weeks than go live with bad data. And if we move it, the agent training falls outside our peak, which my supervisors really want. We'd train in two groups of 70 agents.

ALEX: Alex speaking. I can support a two-week move, but not three. If the duplicates push us to three weeks, I want to go live with the duplicates flagged and fix them in hypercare. And I need to see the impact on customer satisfaction before the steering committee.

MEGAN: Megan. That works for me. So the decision for today: we recommend moving the Brazil go-live by two weeks, the duplicates get fixed in hypercare if needed, and the final approval goes to the steering committee.

ALEX: Alex. Agreed. Lynne should send me the status update with the options and the CSAT impact by Thursday, and she should also approve the 18 thousand dollars for the partner.

MIRIAM: Miriam on the knowledge base. Only 60 of the 180 articles are translated into Portuguese. The agency needs four more weeks. That is still an open risk, and we haven't decided what to do. One option is to go live with the top 80 articles only.

MEGAN: Megan. Let's keep that open and ask Lynne to put it on the steering agenda. One more thing: Isaiah Langer joins as Training Lead next week. Lynne should set up an onboarding one-to-one with him and share the project plan.

ALEX: Alex. Also, Lynne should update the RAID log with the migration and translation risks before the steering meeting.

MEGAN: Megan. To summarise the actions. Lynne: status update to Alex by Thursday, approve the partner budget by Wednesday, onboarding with Isaiah, update the RAID log. Megan: confirm the cleansing duration by Wednesday. Miriam: brief the São Paulo supervisors on the two training groups. Open point: the Portuguese knowledge base. Thanks everyone.
```

---

## E. Upload the project plan

As **Lynne**, upload `demo-assets/Project_Zava_Plan.docx` to OneDrive (*Copilot Demos/Session 2 - Communicate*), if you didn't already do it in setup step 1.

## F. Verify (from setup step 5)

Signed in as **Lynne**, open the recap of *Project Zava weekly sync* in Teams (*Chat* or *Calendar > the meeting > Recap*). Check that the transcript is there and that Copilot answers the question *"What were the decisions?"*. Then run the verification prompt from [TRAINER-SETUP step 5](../../TRAINER-SETUP.md#5-verify-that-copilot-sees-the-session-2-content-10-min).
