# Online Learning Platform Launch: Project Management and Analytics Dashboard
A simulated end-to-end project that combines project management (PMI-style planning, tracking and risk control), generative AI (used at each stage, with a log of what worked and what I corrected) and data analysis (cleaning, modelling and a Power BI dashboard).
> \*\*Note:\*\* This is a portfolio project. All data, names and figures are simulated.
The scenario
Launch an online learning platform with 6 skill courses within 12 weeks on a ₹8,00,000 budget, going live in week 9 and targeting 2,000 sign-ups by the end of week 12.
Tools
Power BI, Excel (Power Query), Gen AI (Claude), GitHub, PM methods (charter, WBS, RACI, risk register, schedule and budget variance tracking).
What I did
Initiation: wrote the project charter (Project-Charter).
Planning: built a 35-task WBS with dependencies, RACI, budget and risk scoring in Excel (Project-Plan.xlsx).
Data: generated 300 simulated sign-up records with deliberate quality issues, then cleaned them (cleaning log).
Dashboard: built a 2-page Power BI report covering project health and business impact (Project-Dashboard.pbix).
Gen AI: logged every prompt, what the AI got right and what I fixed (GenAI-Log).
Dashboard preview
![Project Health](03-Dashboard/1.project health.png)
![Business Impact](03-Dashboard/2.business impact.png)
Key findings
Schedule: the public launch slipped 3 days, driven by UAT running 5 days over plan; later tasks were adjusted to hold the closure date.
Budget: spent ₹7,66,000 of ₹8,00,000 (4.3% under budget). Instructors and marketing ran over, and only ₹35,000 of the ₹1,00,000 contingency was used.
Sign-ups: 285 in the first 4 weeks against a scaled target of 350 (81%). Instagram and Google drove the most sign-ups; Data Analytics was the most popular course.
Engagement: paid learners completed courses at about 62% on average vs about 37% for free learners.
Efficiency: about ₹554 marketing spend per sign-up during the launch period.
The dataset is a scaled-down sample (350 target sign-ups, 17.5% of the full 2,000 goal), so the dashboard shows progress against the sample target.
Data quality issues found and fixed
15 duplicate rows, 22 inconsistent course names, 18 inconsistent traffic-source labels, 12 paid/free case errors, plus blank values in category (4), source (8) and completion (6). Details in the cleaning log.
What I learned
How to turn a project plan into measurable tracking metrics (schedule variance, budget variance, cost per sign-up).
Where gen AI speeds up planning and documentation, and where it needs human checking (totals, dates, formula order, chart scales).
How to turn messy data into a clear dashboard.
Repository structure
01-PM-Documents/   Project-charter.docx, Project-Plan.xlsx
02-Data/           signups\_raw.csv, signups\_clean.csv, Data-Cleaning-Log.md
03-Dashboard/      Project-Dashboard.pbix, 1.project health.png, 2.business impact.png
04-GenAI-Log/      GenAI-Log.md
