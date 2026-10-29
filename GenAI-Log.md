# Gen AI Usage Log

**Project:** Online Learning Platform Launch (simulated)
**AI tool used:** Claude
**Principle:** I used AI to speed up planning, data creation and guidance, then checked its output against the actual data and my own dashboard. Where it was wrong, I corrected it.

## Usage by stage

|Stage|Prompt used (summary)|What the AI did well|What I corrected or rejected|
|-|-|-|-|
|1. Project idea|"Suggest a non-coding portfolio project that combines project management and gen AI, suited to project manager and data analyst roles."|Proposed an end-to-end project: PM documents, a dataset, a Power BI dashboard, an AI log and a GitHub README.|The first scenario was tied to my previous work background. I asked for a neutral theme, and it was changed to an online learning platform launch.|
|2. Project definition and charter|"Give me the project definition (duration, budget, goal, team) and the headings for a charter."|Gave a clear structure: purpose, objectives, scope, out of scope, deliverables, milestones, budget, assumptions, success metrics.|I wrote the charter in my own words using that structure and checked that the budget adds up to ₹8,00,000.|
|3. Project plan workbook|"Create a 35-task WBS in 7 phases with owners, dependencies, planned and actual dates, a RACI, a budget and 12 scored risks."|Produced a consistent plan: 7 phases, dependencies between tasks, a 5-category budget totalling ₹8,00,000, and risks scored as probability × impact.|(a) The budget sheet had a TOTAL row that would have been double-counted in Power BI, so it was removed. (b) Some milestone dates in the charter did not match the schedule (for example UAT end date), so they were corrected to match the workbook.|
|4. Sample data|"Generate about 300 sign-up records with deliberate quality issues (duplicates, inconsistent spellings, blanks)."|Created 300 raw rows with 15 duplicates, inconsistent course and source names, paid/free case errors and blanks.|I checked the cleaned file: 285 rows remain after removing 15 duplicates, and my Power BI total sign-ups card shows 285.|
|5. Data cleaning log|"Write a cleaning log with counts of each fix."|Listed each fix with counts: 22 course names, 18 source labels, 12 paid/free case errors, blank values labelled "Uncategorized" or "Unknown".|Blank completion values (6) were kept blank, not filled, so they do not distort the average completion.|
|6. Dashboard guidance and DAX measures|"Guide me step by step to build a 2-page Power BI dashboard, with measures."|Gave a build order, DAX measures and checkpoint numbers to verify each visual.|(a) I created `Budget Variance %` before `Planned Budget` and got a "cannot be determined" error, so I created `Planned Budget` first. (b) The `Tasks Delayed` measure was missing, so I created it and got 17. (c) The guide expected -4.2% but Power BI showed -4.3%, so I used the value from my dashboard. (d) The weekly sign-ups chart showed the target line on a different scale from the bars, which made it misleading, so I set both axes to 0 to 100.|
|7. README|"Write a README with scenario, tools, findings and a note that data is simulated."|Gave a clear structure and a findings section.|I replaced the placeholders with my own screenshots and checked each finding against my dashboard numbers.|

##### Prompts that worked best

1. Asking for a specific structure (for example "7 phases, 35 tasks, with dependencies") gave more useful output than a general request.
2. Asking for checkpoint numbers at each step let me verify my dashboard against expected values.
3. Asking for deliberately messy data gave me something real to clean.

##### Mistakes the AI made, and how they were caught

##### (some by me, some by checking the AI's own output)

* **Double-counting risk:** a TOTAL row inside a data table would have inflated sums in Power BI. Caught by checking the budget sheet before loading.
* **Date mismatch:** milestone dates in the charter differed from the schedule. Caught by comparing the two documents.
* **Out-of-order instructions:** a measure that depends on another measure was listed before it existed. Caught when Power BI returned an error.
* **Rounding mismatch:** the guide quoted -4.2% where Power BI shows -4.3%. Caught by comparing against my dashboard.
* **Misleading chart:** a secondary axis made the target line look wrong. Caught by reading the chart against the numbers.

##### What I did not use AI for

* Checking every dashboard number against the expected values and my own data.
* Choosing the project theme (removing my previous work background) and the colors ,layout and formatting of the dashboard
* Fixing errors in Power BI(missing measures, the dependencies column type, chart axes).

##### Time comparison (my honest estimate)

|Task|Without AI|With AI|
|-|-|-|
|Project plan (WBS, RACI, budget, risks)|8 to 10 hours|1 to 2 hours(reviewing and understanding)|
|Sample data and cleaning|3 to 4 hours|1 hour|
|Dashboard build|5 to 6 hours|2 to 3 hours|
|README and documentation|4 hours|1 hour|



## Reflection

AI saved me the most time on structure: the plan, the sample data and the step-by-step build order. It was less reliable on details such as totals, dates, the order of formulas, and chart scales, so I verified every number against my own dashboard. I would use AI again for drafting and structure, and I would always check its figures against the source data first.

