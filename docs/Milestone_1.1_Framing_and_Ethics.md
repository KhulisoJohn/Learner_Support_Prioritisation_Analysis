
# Milestone 1.1 Framing & Ethics
  
**Project:** Learner Support Prioritisation Analysis

---

## 1. Problem Framing Note

### Problem Statement

The programme team needs a fair and transparent way to identify learners who may benefit from additional support before their final outcomes are known. Without a structured approach, learners who need help may be overlooked, while others may be unfairly labelled based on incomplete information or personal circumstances.

### Stakeholder

The primary stakeholder is the programme facilitators, who need to identify learners who may benefit from a supportive check-in and determine what assistance they could offer.

### What Does Support Priority Mean?

Support priority means identifying learners who may benefit from early intervention, such as additional academic guidance, a check-in, or help addressing barriers to learning. It is not a judgement of a learner's ability, motivation, or potential.

Any recommendation should be reviewed by a human facilitator. The approach must not automatically penalise learners or deny them opportunities.

### Analytical Question

How can the programme use available learner data to identify learners who may benefit from additional support while avoiding unfair assumptions, profiling, and misleading conclusions?

### Intended Outcome

The goal is to develop a transparent, evidence-informed approach that helps facilitators make better decisions about learner support. The approach should use relevant information available at the time, recognise the limitations of the data, and encourage supportive intervention rather than punishment.

---

## 2. Variable Choices Note

The variables will be reviewed according to their potential usefulness, availability at the decision point, and ethical risks.

### Initial Variable Choices

| Variable | Initial Decision | Reason |
|---|---|---|
| `absences` | Inspect | May indicate a need for a supportive check-in, but absences can have many causes. |
| `studytime` | Inspect | May provide context about study habits, but does not prove effort or motivation. |
| `failures` | Inspect | May indicate previous academic difficulty and a possible need for support. |
| `schoolsup` | Inspect carefully | May help facilitators understand existing support and coordinate assistance. It must not be treated as a penalty. |
| `G1` | Conditional | Consider only if the grade is available before the support decision. |
| `G2` | Conditional | Consider only if the grade is available before the support decision. |
| `G3` | Exclude from live prioritisation | It is the final grade. Using it to make an earlier decision would cause target leakage. It may be considered for retrospective evaluation. |

These are initial choices, not confirmed predictors. The variables must be examined during exploratory data analysis before any prioritisation logic is designed.

### Demographic, Family, and Lifestyle Variables

The following fields will be excluded from individual scoring initially or handled with care.

| Variables | Treatment | Ethical Reason |
|---|---|---|
| `sex` | Exclude | Could result in unfair or discriminatory treatment. |
| `address` | Exclude | Urban or rural residence may act as a proxy for socioeconomic circumstances or access to resources. |
| `Medu`, `Fedu` | Exclude | Parents' education levels could lead to unfair assumptions about family background. |
| `Mjob`, `Fjob` | Exclude | Parents' occupations are not direct measures of a learner's support needs. |
| `romantic` | Exclude | Personal information without an established justification for individual prioritisation. |
| `Dalc`, `Walc` | Exclude | Sensitive personal information that could be misinterpreted or used to stigmatise learners. |
| `age` | Handle with care | Its relevance to support prioritisation has not been established; do not score it initially. |

Other family and lifestyle fields, such as family size, family support, paid classes, and free-time activities, should not automatically be used to assign individual support priority. Their inclusion would require a clear justification and appropriate safeguards.

---

## 3. Ethical Considerations

The analysis will follow these principles:

- **Fairness:** Learners must not be disadvantaged because of demographic, family, or lifestyle circumstances.
- **Transparency:** The reasons for identifying a learner for a check-in must be understandable.
- **Human oversight:** Facilitators must review recommendations and consider the learner's circumstances.
- **Support, not punishment:** Indicators should guide conversations about assistance, not label learners as failures or lacking motivation.
- **Data limitations:** Incomplete or misleading information must not be treated as definitive evidence.
- **Correct timing:** Only information available at the time of the intended decision should be used for live prioritisation.

The dataset is a public student-performance dataset used for practice, not the programme's own learner records. Therefore, any findings must be interpreted cautiously and should not automatically be generalised to the programme's learners.

---

## 4. Conclusion

This milestone establishes the problem, the stakeholder's needs, the meaning of support priority, and the initial variable choices. The analysis will focus on potentially actionable information while avoiding unfair profiling and data leakage.

The next step is to examine the dataset's quality and patterns during **Milestone 1.2** before deciding how learner support could be prioritised.
