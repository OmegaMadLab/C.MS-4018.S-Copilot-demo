# Session 3 – Analyse: from raw data to insight

**Catalogue item:** MS-4018.S05 (Excel), with the Analyst agent in the 90-minute version
**Story:** it's the **Q3 business review** at Contoso Ltd. Sales Operations sent a *draft, not yet validated* Q3 workbook, and you must present the numbers to leadership on Friday. First make the data trustworthy, then find what changed since Q2, show it visually, and turn it into messages. Later, Marketing asks for a quick quality check of product descriptions.

> **Why this story works everywhere:** every role inherits spreadsheets they didn't build, with broken formulas and messy data. Act 5 shows that Excel and Copilot work on **text** too, not just numbers.

## Demo assets

| File | Used in | Rule |
|------|---------|------|
| `excel/Sales_Q3_2026.xlsx`: Read me, Sales (337 rows, table *SalesQ3*), Summary | Acts 1–4 | 🔁 **DUPLICATE** → `Sales_Q3_2026_DEMO.xlsx` |
| `excel/Sales_Q2_2026.xlsx`: Read me, Sales (336 rows, table *SalesQ2*) | Act 3 | 📖 READ-ONLY (only referenced) |
| `excel/Product_Descriptions_Review.xlsx`: 12 descriptions and a 5-criteria rubric | Act 5 | 🔁 **DUPLICATE** → `Product_Descriptions_Review_DEMO.xlsx` |
| `analyst/Service_Level_2026-06…09.csv`: 4 monthly files with the **same structure** | [90] Act 6 | 📖 READ-ONLY. Show only one file to the audience. |

### What's hidden in the data (trainer only, don't reveal it upfront)

**Summary sheet: 3 formula errors**
- **D5:D11 *Achievement %*:** every row divides by `$C$5` (the United States target) instead of its own target.
- **C8 *Brazil target*:** a hard-coded `4500` instead of the `SUMIFS` formula. The real value is about 5,127.
- **B12 *Total net sales*:** `=SUM(B5:B10)` leaves out India.

**Sales sheet: data-quality issues**
- **15 inconsistent category spellings:** *Accesories*, *Personal care*, *Office solutions*, *Home comfort*, *HomeComfort*, *Office*, *Pers. Care*, *accessories*.
- **4 gross margins entered as whole numbers**, which display as **4940.0%** instead of 49.4% (rows for United States/Distributors, Brazil/E-commerce, Australia/Retail, India/Direct B2B).
- **4 blank** *Net sales* cells.
- **2 negative** *Units* values.
- **1 exact duplicate row:** Germany / Retail / Personal Care, 2026-09.

**The Q2 → Q3 story** (after cleaning)
- Net sales up from about **USD 39.9M** to about **USD 42.7M**. **E-commerce** grew about 22% and drives most of the growth (United States +758k, Germany +519k).
- **Brazil Retail:** promo spend **up ~63%** (95 → 155) while net sales went **down ~14%**. This is the *"we spent more and sold less"* insight.
- **Japan Distributors** has the largest decline (−267k).

**Analyst story (CSV files):** **DC Europe (Rotterdam)**, *Home Comfort*, falls below the 92% OTIF threshold from **mid-July** and keeps getting worse to about 87%. Forecast accuracy and stockouts follow the same pattern, with longer lead times. *Office Solutions* at the same DC drops below the 95% target from mid-August. All other DCs are stable at about 96%.

## ✅ Before every delivery (10 min)

- [ ] Open `post-session/Teams_Chat_Messages_Sessions_1-3.html` in a browser tab, ready for the end of the session. If the customer has an AI policy link, paste it in the box at the top.
- [ ] Sign in as **Lynne Robbins** (or any licensed demo user) in an InPrivate window.
- [ ] Delete the previous `_DEMO` copies.
- [ ] 🔁 Duplicate `Sales_Q3_2026.xlsx` → `Sales_Q3_2026_DEMO.xlsx`.
- [ ] 🔁 Duplicate `Product_Descriptions_Review.xlsx` → `Product_Descriptions_Review_DEMO.xlsx`.
- [ ] Open `Sales_Q3_2026_DEMO.xlsx` **in Excel for the web or desktop, saved to OneDrive** (Copilot needs AutoSave on).
- [ ] Backup ready: `BACKUP_Sales_Q3_2026_Dashboard.xlsx` (see [setup step 4](../TRAINER-SETUP.md#4-generate-the-backups-20-min)).
- [ ] **[90]** The pinned conversation `DEMO – Analyst – service levels` is less than a month old.

## Timeline

| 60-min version | 90-min version | Block |
|---|---|---|
| 00:00 – 00:12 | 00:00 – 00:18 | Welcome and [common intro](../README.md#common-introduction-all-sessions) |
| 00:12 – 00:22 | 00:18 – 00:30 | Act 1 – Understand and fix (chat → edit) |
| 00:22 – 00:32 | 00:30 – 00:42 | Act 2 – Clean the data (find errors, plan mode) |
| 00:32 – 00:40 | 00:42 – 00:52 | Act 3 – What changed since Q2? (second file) |
| 00:40 – 00:49 | 00:52 – 01:02 | Act 4 – Visualise: one chart, then a dashboard |
| 00:49 – 00:56 | 01:02 – 01:10 | Act 5 – Not only numbers: check text against rules |
| — | 01:10 – 01:25 | **[90] Act 6 – Analyst: vague vs. precise prompts** |
| 00:56 – 01:00 | 01:25 – 01:30 | Wrap-up: from insight to key messages |

---

## Act 1 – Understand and fix (chat → edit)

🎬 **Say:** *"Sales Ops sent me this Q3 workbook, marked draft. I didn't build it and I present it on Friday. First, I want to understand it."* Show the *Read me* sheet for 20 seconds.

**S3-P1 – Explain the workbook (chat mode):**
```text
Explain what this workbook contains: the purpose of each sheet, the main columns, and how the formulas in the Summary sheet are calculated. Point out anything that looks inconsistent or broken.
```
✅ **Expect:** Copilot spots at least one of the three Summary errors. If it doesn't, follow up:

**S3-P2 – Check the formulas:**
```text
Check every formula in the Summary sheet. For each problem you find, tell me the cell, what is wrong, and what the correct formula should be.
```
✅ **Expect:** the `$C$5` absolute reference, the hard-coded Brazil target and the total that leaves out India.

**S3-P3 – Fix them (switch to edit mode):**
```text
Fix the three problems in the Summary sheet: Achievement % must divide each country's net sales by its own target, the Brazil target must use the same SUMIFS formula as the other countries, and the total must include all countries.
```
🎬 **Teaching point:** *"Chat mode explains and diagnoses. Edit mode changes the file, and that's why we're working on a copy."* Show that *Achievement %* now varies by country.

---

## Act 2 – Clean the data

🎬 **Say:** *"The formulas are fixed, but are the numbers underneath trustworthy? Cleaning data is half the job of an analyst."* Go to the **Sales** sheet.

**S3-P4 – Find the data-quality issues (chat mode):**
```text
Check the SalesQ3 table for data-quality problems: inconsistent category names, impossible or out-of-range values, blank cells, negative numbers and duplicate rows. Give me a table with the issue, the rows affected and a suggested fix. Do not change anything yet.
```
✅ **Expect:** the category variants, the 4940% margins, blanks, negative units and the duplicate.

**S3-P5 – Clean it safely (plan mode, or edit mode that shows a plan):**
```text
Clean the SalesQ3 table: standardise Category so that every value is exactly one of Home Comfort, Office Solutions, Personal Care, Accessories; divide by 100 any Gross margin % above 100%; remove the exact duplicate row; and add a column "Data check" that says "Blank net sales" or "Negative units" for the rows that need a human decision, without changing those values. Show me the plan before applying it.
```
🎬 **Teaching point:** *"Copilot doesn't guess the missing sales. It flags them, and a person decides."*

---

## Act 3 – What changed since Q2? (second file)

🎬 **Say:** *"Leadership will ask one question: what changed since last quarter? Q2 is in another file. I don't copy and paste it, I let Copilot fetch it."*

**S3-P6 – One table from two files:**
```text
Using /Sales_Q2_2026, create a new sheet called "Q2 vs Q3" with one row per Country and Channel and these columns: Net sales Q2, Net sales Q3, Change, Change %, Promo spend Q2, Promo spend Q3, Promo change %. Use the cleaned data in this workbook for Q3. Sort by Change, from the most negative.
```

**S3-P7 – Find the drivers:**
```text
Which countries and channels drove the change in net sales between Q2 and Q3? Show the top 5 positive and the top 5 negative contributors, and highlight any country and channel where promo spend increased but net sales decreased.
```
✅ **Expect:** E-commerce (United States, Germany) on top, Japan Distributors at the bottom, and **Brazil Retail** flagged with promo up and sales down.

---

## Act 4 – Visualise: one chart, then a dashboard

**S3-P8 – One chart that tells one story:**
```text
On the "Q2 vs Q3" sheet, create a chart that compares net sales Q2 and Q3 by channel, with a title that states the key message.
```

**S3-P9 – Dashboard in one prompt:**
```text
Create a dashboard on a new sheet called "Q3 Review" with: net sales vs. target by country, net sales by channel Q2 vs. Q3, promo change % vs. net sales change % by country and channel, and the top 5 declines. Use PivotTables and charts with clear titles that state the key message, and arrange them so they fit on one screen.
```
✅ **Expect:** a one-screen dashboard. Mention that it's built on PivotTables you can edit.
⏱️ **Dashboards take time:** while Copilot works, **move on to Act 5** and come back to show the result. 🛟 If it fails, open `BACKUP_Sales_Q3_2026_Dashboard.xlsx`.

---

## Act 5 – Not only numbers: check text against rules

Open `Product_Descriptions_Review_DEMO.xlsx` (🔁 your copy). Show the **Rubric** sheet and read one bad description aloud (P-1001 or P-1007).
🎬 **Say:** *"Marketing wants every web-shop description checked before the catalogue refresh: no unverifiable claims, real benefits, complete specs. That's 12 rows today, but it could be 1,200. Same pattern for contracts, policies, job ads or survey comments."*

**S3-P10 – Score against a rubric (edit mode):**
```text
Review each product description in the ProductDescriptions table against the criteria in the Rubric sheet. Add these columns to the right of the table: Clarity (1–5), Customer benefit (1–5), Claims compliance (1–5), Key specs completeness (1–5), Brand voice (1–5), Overall score (average), Main issue (max 15 words), Suggested rewrite of the first sentence (max 25 words). Do not change the original descriptions.
```
✅ **Expect:** low compliance for P-1001, P-1006, P-1007, P-1010 and P-1012 (superlatives, "100% eco-friendly", medical claims). High scores for P-1002, P-1005, P-1008 and P-1011.
🎬 **Teaching point:** *"Scores are suggestions. People decide. Ask Copilot why it gave a score."*

---

## [90] Act 6 – Analyst: vague vs. precise prompts

🎬 **Say:** *"Copilot in Excel is great inside one workbook. When I have several files, in different formats, and need reasoning plus code, I go to Analyst. Here are 4 monthly service-level exports from our distribution centres, all with the same structure."* Open **one** CSV for 20 seconds to show the columns.

**S3-A1 – The vague prompt (run live, new Analyst conversation, attach the 4 CSV files):**
```text
Analyse these service level reports and tell me how we are doing.
```
🎬 While it runs, open the pinned conversation **DEMO – Analyst – service levels** and show the precise prompt:

**S3-A2 – The precise prompt (already run and pinned):**
```text
Analyse the attached weekly service level reports for June, July, August and September 2026 (by warehouse and category).
Definitions and thresholds: OTIF target 95% (below 92% is critical); fill rate target 98%; forecast accuracy target 80%.
1. Show the monthly average of OTIF, fill rate and forecast accuracy by warehouse in a table.
2. Flag every warehouse and category combination that is below the OTIF target for 3 or more consecutive weeks, and say when it started.
3. Identify the most likely drivers of the OTIF drop using lead time, stockouts and forecast accuracy, and show the correlations.
4. Summarise the results in maximum 5 bullets for a supply chain director.
5. Create a line chart of OTIF by warehouse over time.
Show me the code you used for each step.
```
✅ **Expect:** DC Europe (Rotterdam) / Home Comfort flagged from mid-July, critical below 92%. Office Solutions at the same DC below target from mid-August. Strong correlation with forecast accuracy and stockouts.
🎬 **Teaching point:** compare the vague result with the precise one. *"Vague prompts give different answers every time. Definitions, thresholds and steps give answers you can repeat and trust. And you can check the code."*

**S3-A3 – Make it repeatable (same pinned conversation, live):**
```text
Write the exact prompt I should use next month when the October report arrives, so that the analysis uses the same definitions, thresholds, steps and output format and the results are comparable with this one.
```

---

## Wrap-up: from insight to key messages (4 min)

Back in `Sales_Q3_2026_DEMO.xlsx` with the finished **Q3 Review** dashboard.

**S3-P11 – Key messages for leadership:**
```text
Write the 3 key messages for our leadership team from the "Q3 Review" dashboard. Each message must be one sentence with the supporting number, and suggest the best chart type to show it on a slide.
```
🎬 **Takeaways:**
1. **Understand before you change:** chat mode first, edit mode on a copy.
2. **Trust comes from clean data:** let Copilot find the issues, and keep the human decision for the ambiguous ones.
3. **Reference other files instead of copying.**
4. **One chart, one message.** Dashboards are the destination.
5. **[90] Precise prompts give repeatable analysis.**

## After the session: share the take-away message

Open [Teams_Chat_Messages_Sessions_1-3.html](../post-session/Teams_Chat_Messages_Sessions_1-3.html) in a browser, click **Copy message** on *Session 3 – Analyse* and paste it into the meeting chat. The message contains the official guides, how to save, share and schedule prompts, and the reusable versions of today's prompts.

## Reusable prompt patterns (reference)

```text
Explain what this workbook contains: the purpose of each sheet, the main columns, and how the formulas in [sheet] are calculated. Point out anything that looks inconsistent or broken.
```
```text
Check the [table] for data-quality problems: inconsistent names, out-of-range values, blanks, negatives and duplicates. Give me a table with the issue, the rows affected and a suggested fix. Do not change anything yet.
```
```text
Using /[other file], create a new sheet with one row per [keys] and columns: [measures for each period], Change, Change %. Sort by [column].
```
```text
Create a dashboard on a new sheet called "[name]" with: [measure by dimension], [comparison], [breakdown], [top N]. Use PivotTables and charts with titles that state the key message.
```
```text
Review each [item] in the table against the criteria in [sheet]. Add columns: [criterion 1–n] (1–5), Overall score, Main issue, Suggested improvement. Do not change the original data.
```
```text
Analyse [files]. Definitions and thresholds: [KPI = target, critical level]. 1) [trend]; 2) [flag rule]; 3) [drivers]; 4) summary in max [5] bullets for [audience]; 5) [chart]. Show me the code you used.
```
