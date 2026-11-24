# Mobius Claim Check

Use this skill before sharing a slide or an AI answer to see which claims your sources support and get wording you can paste back into the draft.

SolarPlexus Mobius helps people trace AI answers to their sources. This skill shares one part of that workflow with anyone reviewing a claim. Paste a draft or question and the relevant figures or excerpts. The instructions fit in [one file](mobius-claim-check/SKILL.md).

## Try it on a real product question

After reviewing the Stack Overflow Developer Survey, I wanted to know how much the findings actually said about demand for Mobius. Here is the question, with the relevant source notes included so anyone can repeat the review.

### Input

> My question after reading a developer survey: “So this confirms theres a market for my mobius project?” SolarPlexus Mobius helps people check AI answers against sources.
>
> S1 — Stack Overflow, 2025 Developer Survey, *Accuracy of AI tools*. On the accuracy question, 46% of respondents expressed distrust and 33% expressed trust.
>
> S2 — Same survey, *AI tools in the development process*. On the usage question, 84% reported current or planned use of AI tools for development.

[Read the original survey results](https://survey.stackoverflow.co/2025/ai/)

### Output from the skill

Use the survey to justify testing SolarPlexus Mobius with developers. Demand for a tool that checks AI answers against sources is still unverified.

| Claim | Verdict | Evidence |
|---|---|---|
| More respondents distrusted AI tools’ accuracy than trusted it. | **Supported** | On the 2025 accuracy question, 46% expressed distrust and 33% expressed trust, a gap of 13 percentage points (46 − 33). [S1] |
| Most respondents used or planned to use AI tools for development. | **Supported** | On the usage question, 84% reported current or planned use. [S2] |
| Developers who use AI tools also distrust their accuracy. | **Unverified** | The 46% distrust figure [S1] and the 84% current-or-planned-use figure [S2] come from separate questions. A breakdown of accuracy responses by current use would show the overlap. |
| Developers will pay for SolarPlexus Mobius to check AI answers against sources. | **Unverified** | S1 measures trust in accuracy and S2 measures tool use or plans. A paid pilot would show whether developers choose Mobius for this task at a stated price. |

**Ready-to-use wording**

In Stack Overflow’s 2025 Developer Survey, 46% of respondents to the accuracy question distrusted AI tools’ accuracy and 33% trusted it [S1], while 84% of respondents to a separate question used or planned to use AI tools for development [S2]. Would developers pay for SolarPlexus Mobius to check AI answers against sources during their work?

## What changed after testing

The first reviews cited the evidence in the table, but the citations disappeared when I copied the closing paragraph. I changed the instructions to cite each factual sentence in the rewrite. I also added rules for revised estimates, overlapping groups, missing values, and rounding once from the original figures.

| Fresh case | What the revised skill caught |
|---|---|
| Stack Overflow survey | Different questions measure AI use and trust. Neither question measures willingness to pay for Mobius. |
| U.S. payroll newsletter | A 100,000-job upward revision belonged to November and December. The February publication date did not make it February hiring. |
| Ramp AI Index | Rounding the underlying vendor shares after subtraction gave a 4.21-point gap. Vendor shares overlap, and an unreported share cannot establish zero paying customers. |

## Install in Codex

1. Download or clone this repository. Copy the entire `mobius-claim-check` folder into `.agents/skills/` at the root of the project where you use Codex. The file should end up at `.agents/skills/mobius-claim-check/SKILL.md`.
2. Open a fresh Codex session in that project. Type `$mobius-claim-check`, followed by your draft and its source excerpts.
3. To try automatic discovery, ask “Can I say this in my slide based on these figures?” and paste the same input.

[Codex skill installation documentation](https://developers.openai.com/codex/skills/)
