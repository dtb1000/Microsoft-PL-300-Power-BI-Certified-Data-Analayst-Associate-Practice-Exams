# PL-300: Microsoft Power BI Data Analyst Last 4-Days Study Plan

A plan for the final four days before PL-300: one timed mock a day, focused review of your weakest domain in the question bank, and a dress rehearsal the day before.

## The four days at a glance

Day 2 carries two mocks so the day before the exam can stay light; it ends early, so you sit the exam rested.

## Day-by-day checklist

Each mock takes 80 minutes plus about an hour of review. Mark it straight away, tag every miss by domain, and spend the review on the domain where you missed most. Ticks are saved in this browser.

- [ ] **Day 1.** Take [Mock Exam 1](https://claude.ai/artifact/KxheDUHMd8aYk5VvPm37Bb) (80 minutes). Mark it, then rebuild every missed DAX or Power Query question in Power BI Desktop. Spend 30 minutes in the [question bank](https://claude.ai/artifact/PjtWcxqeny22qASVheSfxE) on your weakest domain.
- [ ] **Day 2.** Take [Mock Exam 2](https://claude.ai/artifact/YKj3DcwzHAgNvNDkertzV4) in the morning and [Mock Exam 3](https://claude.ai/artifact/Dy5PQhVj7QggaBKeSEhbcg) in the afternoon. Review the Model domain: CALCULATE filter behaviour, time intelligence and semi-additive measures, using the bank filtered to Model the data.
- [ ] **Day 3.** Take [Mock Exam 4](https://claude.ai/artifact/AiQp7RAYZocWNG532geppm). Review Manage and secure: workspace roles, RLS, gateways, refresh limits, sharing and labels. Then try the [official practice assessment](http://aka.ms/PL300-PA), and finish with the bank’s “Not right last time” questions.
- [ ] **Day 4.** Take [Mock Exam 10](https://claude.ai/artifact/8YRGMmD1XPkhT2n54Eppfy) as a dress rehearsal. Reread the cheat sheet below and walk through the [exam sandbox](https://aka.ms/examdemo). Stop studying by early evening.
- [ ] **Exam day.** Have your ID ready and start check-in early. Budget about 2 minutes a question, flag and move on when stuck, and keep 20 minutes for the case study.

Scoring guide: 30 or more out of 40 on a mock means you are on track; 26–29 means drill that mock’s weakest domain again before the next one; under 26, redo the missed questions before starting the next mock.

If you have more than four days left, take one mock a day in order, keep Mock 10 for the day before the exam, and use the question bank between mocks.

## Exam format and domain weights

The live exam has 40–60 questions in 100 minutes and needs a scaled 700 out of 1,000 to pass. The mocks have 40 questions in 80 minutes, which keeps the same pace.

| Item | Live exam | Mocks |
| --- | --- | --- |
| Questions | Typically 40–60, including at least one case study | 40 each, including a 3-question goal series and a 6-question case study |
| Time | 100 minutes | 80 minutes (about 2 minutes a question) |
| Pass mark | 700 on a 1–1,000 scaled score | Aim for 30/40 (75%) |
| Partial credit | Multi-part items usually score per correct part | Strict or partial-credit scoring, chosen at the start |

| Domain | Weight |
| --- | --- |
| Prepare the data | 25–30% |
| Model the data | 25–30% |
| Visualize and analyze the data | 25–30% |
| Manage and secure Power BI | 15–20% |

Question types match the live exam: single choice, multiple choice (“choose two”), sequence, code completion, Yes/No statements, goal series (you answer each once and can’t go back) and case studies (you can’t return after leaving one).

## Two decisions the exam tests constantly

Storage mode is chosen per table, so one composite model can mix all four. Whether a source needs a gateway depends only on where the source lives; a Fabric capacity or a Premium workspace never removes the need for one.

## High-yield cheat sheet

Reread this the evening before the exam and again before check-in.

| Topic | What to remember |
| --- | --- |
| **Storage modes** | Import = fastest, needs refresh. DirectQuery = live, slower, data stays at the source. Dual = dimension shared by Import and DirectQuery tables. Direct Lake = Delta tables in OneLake, Fabric capacity, no import copy. |
| **Privacy levels** | Private: combine with nothing. Organizational: combine with Organizational, never sent to Public. Public: anything. |
| **Merge join kinds** | Left outer (all left), Right outer, Full outer, Inner (matches only), Left anti (left with no match), Right anti. Fuzzy matching for near-identical text. |
| **Query relationships** | Reference = follows the original’s changes. Duplicate = independent copy. Enable load off = staging only. Include in report refresh off = keep data, skip refresh. |
| **Profiling** | Top 1,000 rows by default; switch to the entire data set. Distinct = different values; unique = values appearing once. |
| **Relationships** | One active path between tables; extra paths are inactive (use USERELATIONSHIP). Both direction only when needed; CROSSFILTER for one measure; TREATAS for a virtual relationship. |
| **Date table** | Unique, contiguous, no blanks, same time on every value; mark as a date table; turn off Auto date/time. |
| **CALCULATE** | A boolean filter replaces filters on that column; KEEPFILTERS intersects; FILTER is needed to test a measure; REMOVEFILTERS and ALL clear; ALLSELECTED keeps slicers; ALLEXCEPT keeps the listed columns. |
| **Time intelligence** | TOTALYTD (fiscal: “06-30”), SAMEPERIODLASTYEAR, DATEADD (shift by n units), PARALLELPERIOD and PREVIOUSYEAR (whole period), DATESINPERIOD (rolling window), DATESBETWEEN (fixed range). |
| **Semi-additive** | LASTDATE (every day has data), LASTNONBLANK (gaps), CLOSINGBALANCEMONTH and OPENINGBALANCEMONTH. |
| **Calculation groups** | SELECTEDMEASURE(); ISSELECTEDMEASURE to skip measures; Discourage implicit measures turns on; format string expressions per item; precedence between groups. |
| **Performance** | Remove unused columns and rows, reduce granularity, use integer keys, split date-time columns, avoid unneeded bidirectional filters. Performance Analyzer: DAX query, Visual display, Other (waiting). |
| **Visuals** | Waterfall = movement from start to end. KPI = value, target and trend. Gauge = value against a maximum. Scatter = correlation and clusters. Key influencers = drivers. Decomposition tree = user-ordered breakdown. |
| **Report features** | Bookmarks: Data, Display, Current page, Selected visuals. Drillthrough: Keep all filters, Cross-report, back button. Tooltip page: Allow use as tooltip plus a Tooltip canvas. Edit interactions is set on the source visual. |
| **Forecast and analytics** | Forecast: line chart, continuous date axis, no legend. Anomaly detection: line chart time series. Error bars: upper and lower bound fields. Lines can take their value from measures. |
| **Automatic page refresh** | DirectQuery only; fixed interval, or change detection (one measure per model, on capacity); the admin sets the minimum interval. |
| **Copilot** | Narrative visual (summarises the page, accepts a custom prompt), create a report page, suggest content for a page, summarise the semantic model. Needs a paid Fabric capacity (F2+) or Premium P, enabled by the admin. |
| **Paginated reports** | Print-ready, many pages, repeating headers, run-time parameters; built in Power BI Report Builder. |
| **Workspace roles** | Admin: everything, including deleting the workspace and adding Admins. Member: adds Members, Contributors and Viewers; publishes and updates the app. Contributor: creates and edits content. Viewer: view only. |
| **Row-level security** | Define roles in Desktop and assign users or security groups in the service. Dynamic with USERPRINCIPALNAME(). Applies to Viewers and app users only. Roles are additive. Test with View as, or Test as role in the service. |
| **Permissions and licences** | Build = create reports or use Analyze in Excel on a model. Free users need content on F64+ or Premium P capacity. Share with reshare and build cleared for least privilege. |
| **Refresh and gateway** | Gateway for on-premises sources; none for public cloud sources; a VNet data gateway for private endpoints. Standard mode for shared use and DirectQuery. 8 refreshes a day on Pro; 48 on Premium, PPU or Fabric. |
| **Distribution** | App (audiences), dashboard (tiles from many reports, data alerts on card, KPI and gauge tiles), subscriptions (scheduled or after refresh, dynamic per recipient), Teams tab, SharePoint Online web part. Never Publish to web for internal data. |
| **Governance** | Promote: anyone with write permission. Certify: users the admin authorises. Sensitivity labels persist on export and can be inherited downstream. |

## Sources

[Official PL-300 study guide](https://learn.microsoft.com/en-us/credentials/certifications/resources/study-guides/pl-300): skills measured as of April 20, 2026, exam facts and pass mark, checked on 9 November 2026.

Unofficial practice material, not affiliated with or endorsed by Microsoft. Written against the PL-300 skills measured as of April 20, 2026, and last reviewed on 9 November 2026.