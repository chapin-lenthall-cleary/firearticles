# Violence, ideology, and gender wording by survey year, 2020–2026

Years below are **survey/data years**, not the year printed on the rankings
report cover. For example, the 2025 survey produced the 2026 College Free
Speech Rankings, and the 2026 survey produced the 2027 rankings.

## Year-by-year map

| Data year | Violence | Ideology | Gender |
|---:|---|---|---|
| 2020 | V1 | I1 | G1 |
| 2021 | V2 | I2 | G1 |
| 2022 | V2 | I2 | G2 |
| 2023 | V2 | I2 | G2 |
| 2024 | V2 | I2 | G3 |
| 2025 | V3 | I2 | G3 |
| 2026 | V3 | I2 | G3 |

The version definitions below give the question and answer wording. Minor
punctuation differences in the published reports (a colon versus a question
mark after the prompt, or a period versus a question mark after the item) are
not treated as substantive changes.

## Violence

### V1 — 2020

**Question:** “How acceptable would you say it is for students to engage in
the following action to protest a campus speaker: Using violence to stop a
speech or event on campus?”

**Answers:**

1. Always acceptable
2. Sometimes acceptable
3. Rarely acceptable
4. Never acceptable

Original public-data field: `q17` (the published questionnaire numbers the
item Q18). Megafile field: `act_viol`.

### V2 — 2021, 2022, 2023, and 2024

**Prompt:** “How acceptable would you say it is for students to engage in the
following action to protest a campus speaker?”

**Item:** “Using violence to stop a campus speech.”

**Answers:**

1. Always acceptable
2. Sometimes acceptable
3. Rarely acceptable
4. Never acceptable

Original public-data field: `violence`. Megafile field: `act_viol`.

### V3 — 2025 and 2026

**Prompt:** “How acceptable would you say it is for students to engage in the
following actions to protest a campus speaker?”

**Item:** “Using violence to stop a campus speech.”

**Answers:**

1. Always acceptable
2. Sometimes acceptable
3. Rarely acceptable
4. Never acceptable

The only change from V2 is singular **action** becoming plural **actions**.
The 2025 original public-data field is `violence`; the 2026 raw field is
`q17`. Both are `act_viol` in the megafile.

## Ideology

### I1 — 2020

**Question:** “Using a seven-point scale from extremely liberal—point 1—to
extremely conservative—point 7—where would you place yourself on this
scale?”

**Answers:**

1. Extremely liberal
2. Liberal
3. Slightly liberal
4. Moderate
5. Slightly conservative
6. Conservative
7. Extremely conservative
8. Something else

The published topline also records refused/no answer. The 2020 public-data
field is `politicalLeaning`. The megafile harmonizes the seven scale positions
to `ideo=1` through `ideo=7`; “Something else” and missing are not retained as
a separately analyzable substantive category in the packaged 2020 `ideo`
values.

### I2 — 2021, 2022, 2023, 2024, 2025, and 2026

**Primary question:** “Using the following scale, how would you describe your
political beliefs?”

**Primary answers:**

1. Very liberal
2. Somewhat liberal
3. Slightly liberal
4. Moderate, middle-of-the-road
5. Slightly conservative
6. Somewhat conservative
7. Very conservative
8. I do not identify as a liberal or a conservative
9. Haven’t thought much about this

Respondents selecting “I do not identify as a liberal or a conservative” were
asked:

**Follow-up question:** “Which of the following best describes your political
beliefs?”

**Follow-up answers:**

1. Democratic Socialist
2. Libertarian
3. Other / Something else

“Something else” is explicitly a write-in in the later questionnaires. The
megafile flattens the primary and follow-up responses into `ideo`:

1. Very liberal
2. Somewhat liberal
3. Slightly liberal
4. Moderate, middle-of-the-road
5. Slightly conservative
6. Somewhat conservative
7. Very conservative
8. Democratic Socialist
9. Libertarian
10. Haven’t thought much about this
11. Something else

Source fields vary by year: `ideology` plus `ideology_write` in 2021;
`ideo` plus a follow-up/write-in field in 2022–2023; `ideo` in the later
public files; and `demographics_politicalIdeology` in the 2026 raw file.

For 2024–6, the released CFSR instruments do not print this College Pulse
profile question. Their codebooks label the field “Political ideology” and
retain the same answer architecture; the full I2 prompt is directly printed
in the 2021–2023 reports.

Two source-data cautions matter when interpreting the packaged megafile:

- The questionnaire distinguishes Libertarian from “Haven’t thought much
  about this,” but the packaged 2022 data contain no `ideo=10` observations,
  despite the megafile codebook listing that category.
- The supplied 2026 data dictionary lists Democratic Socialist and
  Libertarian, but the 2026 data contain no `ideo=8` or `ideo=9` observations.
  The available files do not establish whether those choices were omitted in
  administration or collapsed upstream.

These are data/coding cautions, not documented wording changes.

## Gender

### G1 — 2020 and 2021

**Question:** “Which of the following genders do you most identify with?”

**Answers:**

1. Male
2. Female
3. Non-binary

The exact 2020 stem is not printed in the 2020 CFSR report. The wording above
is the continuing College Pulse profile question used in the harmonized
codebook; FIRE’s 2020 analysis independently confirms the three male, female,
and non-binary groups. In the 2020 public file the third category is stored as
`gender=6`; the megafile harmonizes it to `gender_bin=3`.

### G2 — 2022 and 2023

**Question:** “Which of the following genders do you most identify with?”

**Answers:**

1. Male
2. Female
3. Nonbinary
4. Agender
5. Genderqueer/Genderfluid
6. Unsure
7. Declined to say

### G3 — 2024, 2025, and 2026

**Question:** “Which of the following genders do you most identify with?”

**Answers:**

1. Male
2. Female
3. Nonbinary
4. Agender
5. Genderqueer/Genderfluid
6. Unsure

“Declined to say” is no longer retained as a separate substantive response in
the released files. The megafile collapses Nonbinary, Agender,
Genderqueer/Genderfluid, and Unsure into `gender_bin=3`, labeled “Gender
non-conforming”; missing/no response is `gender_bin=99`.

