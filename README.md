# PL-300 Mock Exams

Five free, timed, interactive practice exams for **Microsoft Exam PL-300: Microsoft Power BI Data Analyst**. Each exam runs in the browser as a single HTML file, with no installation, sign-in or server-side code.

**Currency of the material:** the questions follow the PL-300 \*skills measured as of April 20, 2026\*. They were last reviewed on **9 November 2026**, against the official study guide (page last updated 30 October 2026). At that point no newer skills outline had been announced. The material is intended to be current through **December 2026**, but Microsoft updates the exam periodically. Check the \[study guide's change log](https://learn.microsoft.com/en-us/credentials/certifications/resources/study-guides/pl-300) before relying on it after that date.

## Contents

* [What's included](#whats-included)
* [How to use the exams](#how-to-use-the-exams)
* [How closely the mocks match the real exam](#how-closely-the-mocks-match-the-real-exam)
* [What the questions are based on](#what-the-questions-are-based-on)
* [Date range of the referenced material](#date-range-of-the-referenced-material)
* [Known bugs and limitations](#known-bugs-and-limitations)
* [Repository structure](#repository-structure)
* [Testing](#testing)
* [Reporting a mistake](#reporting-a-mistake)
* [Disclaimer](#disclaimer)
* [License](#license)

## What's included

|Exam|Case study|Prepare|Model|Visualize|Manage|
|-|-|-|-|-|-|
|[Mock Exam 1](exams/mock-exam-1.html)|Northwind Pharma Distribution|10|9|11|10|
|[Mock Exam 2](exams/mock-exam-2.html)|Fabrikam Biotech Labs|12|11|11|6|
|[Mock Exam 3](exams/mock-exam-3.html)|Contoso Outdoor Retail|9|12|13|6|
|[Mock Exam 4](exams/mock-exam-4.html)|Litware Logistics|10|15|9|6|
|[Mock Exam 5](exams/mock-exam-5.html)|Proseware Clinical Research|10|10|11|9|
|**All five**||**51 (25.5%)**|**57 (28.5%)**|**55 (27.5%)**|**37 (18.5%)**|

Across all 200 questions, the mix matches Microsoft's published domain weights: 25–30% for each of the first three domains and 15–20% for Manage and secure. Individual exams vary, so take all five for balanced coverage.

Each exam has:

* **Questions 1–31.** Standalone questions you can move between freely and flag for review.
* **Questions 32–34.** A goal series: the same goal with three different solutions. Each answer is final once you continue.
* **Questions 35–40.** A case study with an exhibit diagram of the company's data environment.
* **An 80-minute timer** that submits the exam automatically at zero.
* **A results page** with your score out of 40, a breakdown by domain, and a colour-coded answer sheet.
* **A review mode** showing your answer, the correct answer and an explanation for every question. You can filter it to the questions you missed.

Question types: single choice (140), goal series Yes/No (15), Yes/No statements (15), code completion with DAX dropdowns (13), multiple choice "choose two/three" (12), sequence (4) and matching (1).

## How to use the exams

### Option 1: GitHub Pages (recommended)

1. Push this repository to GitHub.
2. Go to **Settings > Pages**.
3. Under **Build and deployment**, set **Source** to *Deploy from a branch*, choose `main` and `/ (root)`, and select **Save**.
4. After a minute, open `https://<your-username>.github.io/<repository-name>/`. The landing page links to all five exams.

### Option 2: Run locally

Download or clone the repository and open `index.html` in a modern browser (Chrome, Edge, Firefox or Safari). No build step is needed.

If your browser blocks storage for local files, the exams still work but progress isn't saved between visits. Serving the folder fixes this, for example with `python3 -m http.server` and then opening `http://localhost:8000`.

### Taking an exam

1. Open an exam and choose a scoring mode:

   * **Strict:** a question with several parts scores only when every part is right.
   * **Partial credit:** each correct part earns its share of the point. This is closer to how Microsoft scores, with the differences listed under [Known bugs and limitations](#known-bugs-and-limitations).
2. Select **Start exam**. Answer with the radio buttons, checkboxes, dropdowns or Yes/No buttons.
3. Use the **answer sheet** to jump between questions in the current section. Filled circles are answered, amber rings are flagged, and dashed circles are locked or not yet available.
4. At question 31, review the section and select **End section**. You can't return to questions 1–31 after this, which mirrors the live exam.
5. Answer the goal series, then the case study, and select **Finish exam**.
6. Read your score and domain breakdown, then select **Review answers**. Selecting a circle on the results answer sheet jumps to that question's explanation.

**Suggested schedule:** one mock a day, marked straight away, with the following review spent on your weakest domain. Aim for **30 or more out of 40** before exam day. Mock 5 is designed as a final dress rehearsal.

**Progress:** answers, flags and the remaining time are saved in your browser's local storage after every change. You can close the page and resume later. **Retake exam** clears the attempt.

## How closely the mocks match the real exam

||Live PL-300 exam|These mocks|
|-|-|-|
|Questions|Typically 40–60, including at least one case study|40, including a goal series and a case study|
|Time|100 minutes|80 minutes, so the pace of about 2 minutes per question stays the same|
|Passing score|700 on a scaled score of 1–1,000|Target of 30/40 (75%); a raw score, not scaled|
|Multi-part scoring|Usually one point per correct part, no penalty for guessing|Strict (all or nothing) or partial credit (see limitations)|
|Locked sections|Goal series and case studies can't be revisited|Same|

## What the questions are based on

* [**Study guide for Exam PL-300**](https://learn.microsoft.com/en-us/credentials/certifications/resources/study-guides/pl-300), skills measured as of April 20, 2026. Every question maps to one of its four domains and their listed skills.
* [**Exam scoring and score reports**](https://learn.microsoft.com/en-us/credentials/certifications/exam-scoring-reports), for the 700 pass mark, partial credit and the no-penalty-for-guessing rule.
* **Power BI and Microsoft Fabric documentation on Microsoft Learn**, for feature behaviour such as storage modes, DAX functions, RLS, gateways, refresh limits, Copilot and visual calculations.

All questions, scenarios and company names are original practice material written for this project. They are **not** taken from the live exam, and no exam content or "brain dumps" were used. The companies in the case studies (Northwind, Fabrikam, Contoso, Litware, Proseware) are Microsoft's usual fictitious example names.

## Date range of the referenced material

|Item|Date|
|-|-|
|Skills outline the questions follow|Effective **April 20, 2026**|
|Official study guide last updated (as checked)|30 October 2026|
|Exam scoring page last updated (as checked)|27 May 2025|
|Feature behaviour described in explanations|As documented on Microsoft Learn, checked **November 2026**|
|Last full review of all questions and answers|**9 November 2026**|
|Intended to remain current until|**December 2026**, unless Microsoft publishes a new skills outline earlier|

Scope decisions made during the November 2026 review:

* **Q\&A visual removed.** The Q\&A feature is not in the April 2026 skills measured, and community reports say it is retiring in December 2026. Questions that relied on it were replaced, and it no longer appears as an answer option.
* **Quick insights removed** as an answer option, because it is not in the April 2026 skills measured.
* **Copilot** questions assume a paid Fabric capacity (F2 or higher) or Premium P capacity, with Copilot enabled by the tenant admin.
* **Direct Lake**, **visual calculations**, **calculation groups in Power BI Desktop** and **DAX query view** are treated as current features, because the skills outline lists them.

If Microsoft changes the skills outline, check these areas first: Copilot features, Direct Lake, licensing and capacity thresholds (F64 for Free-licence viewers), refresh limits (8 a day on Pro, 48 on Premium, PPU and Fabric), and any retired visuals.

## Known bugs and limitations

None of the issues below stops an exam from working; they are known gaps between the mocks and the live exam, or rough edges in the interface.

### Scoring

1. **Partial-credit mode is harsher than Microsoft on "choose two/three" questions.** A wrong pick cancels out a right one, so one right plus one wrong scores 0. Microsoft deducts nothing for wrong answers.
2. **Every question is worth one point.** On the live exam, multi-part questions are usually worth one point per part, so they carry more weight there than here.
3. **Scores are raw, not scaled.** 30/40 is a readiness target, not a conversion of Microsoft's 700/1,000.
4. **The scoring mode is fixed once an attempt starts.** To switch modes, select **Retake exam** and choose again.

### Saving and timing

5. **Progress is stored per browser and per device.** It doesn't follow you to another browser or computer, it isn't kept in private or incognito windows, and clearing site data deletes it.
6. **The timer keeps counting while the page is closed,** like the live exam. If you reopen an attempt after its time has run out, it is submitted automatically.

### Content and display

7. **Answers are visible in the page source.** The exams are self-study tools and are not protected against peeking.
8. **The domain mix varies between exams.** For example, Mock 4 has 15 Model questions and 6 Manage questions. Only the full set of five matches the official weights.
9. **Fonts load from Google Fonts.** Offline, the pages fall back to system fonts; nothing else needs a network connection.
10. **Exhibit diagrams are scaled to fit.** On small phone screens, labels in the case-study diagrams become small. Zoom in, or use a tablet or laptop for the case studies.

### Accessibility

11. **The page re-renders after each answer.** Keyboard focus is restored, but screen readers may re-announce content. The exams have not been tested with a screen reader.

### Interface details

12. **Sequence questions block reusing an action.** An action already chosen for one step is greyed out for the others, and you can't pick the same action twice. That is correct for these questions, but it differs from the drag-and-drop interface of the live exam.
13. **English only, with no in-page theme switch.** The pages follow your operating system's light or dark mode.

To report a new bug, see [Reporting a mistake](#reporting-a-mistake).

## Repository structure

```text
pl300-mock-exams/
├── README.md              This file
├── LICENSE                MIT license
├── CHANGELOG.md           Release notes and review changes
├── .nojekyll              Tells GitHub Pages to serve files as they are
├── index.html             Landing page that links to the five exams
└── exams/
    ├── mock-exam-1.html   Case study: Northwind Pharma Distribution
    ├── mock-exam-2.html   Case study: Fabrikam Biotech Labs
    ├── mock-exam-3.html   Case study: Contoso Outdoor Retail
    ├── mock-exam-4.html   Case study: Litware Logistics
    └── mock-exam-5.html   Case study: Proseware Clinical Research
```

Each exam file is self-contained, with its HTML, CSS, JavaScript, questions and SVG diagrams all inline. To edit a question, search the file for its number, for example `{n:12,`. Every question object has:

* `stem`: the question text.
* `options`: the answer options.
* `answer` (or `answers`, `blanks`, `items` or `statements`, depending on the question type): the correct answer.
* `key`: the answer shown in review.
* `why`: the explanation.
* `d`: its domain, where `P`, `M`, `V` and `S` are the four domains in order.

## Testing

Before release, every exam was tested end to end in Chromium with Playwright:

* All 40 questions answered correctly through the real interface (radio buttons, checkboxes, dropdowns and Yes/No buttons) scores 40/40 in strict mode.
* A fully blank attempt scores 0 in partial-credit mode, and all 40 review cards render.
* Section locks, goal-series locks, the cap on "choose two/three" selections, flagging, jumping via the answer sheet, saving and resuming after a reload, and automatic submission when time runs out all work.
* No JavaScript errors were raised.
* Layout was checked on a 1280-pixel desktop and a 390-pixel phone, in light and dark mode.

## Reporting a mistake

If you find a wrong answer, an outdated feature or a typo, open an issue with:

* the exam number and question number;
* what you think is wrong;
* a link to Microsoft documentation that supports the correction, if you have one.

## Disclaimer

This is unofficial study material. It is not affiliated with, endorsed by or sponsored by Microsoft. Microsoft, Power BI, Microsoft Fabric, Microsoft Entra, Microsoft Purview and Microsoft Teams are trademarks of the Microsoft group of companies.

Passing these mocks doesn't guarantee a pass on the live exam. Always check the official study guide for the current skills measured.

## License

Released under the [MIT License](LICENSE).

