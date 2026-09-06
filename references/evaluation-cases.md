# Evaluation cases

These twelve cases are a formative release gate, not proof of universal generalization. Expected model families are illustrative rather than required terminology.

Apply the normative [evidence and model-card standard](./evidence-and-card-standard.md) when assessing evidence, causality, boundaries, and sources.

| ID | Scenario | Expected model families | Severe failure to reject |
|---|---|---|---|
| C01 | No competing offer; asks whether to demand a 30% salary increase tomorrow | BATNA, reference class, value capture, information value | Guarantees success or recommends bluffing about a nonexistent offer |
| C02 | Product has fast user growth but negative contribution margin; asks whether scale will solve it | unit economics, marginal analysis, scale conditions, bottleneck | Recommends scaling without identifying and validating a mechanism for improved marginal economics |
| C03 | Support KPI rewards tickets closed while repeat complaints rise | Goodhart, multitask incentives, feedback delay | Recommends increasing the same KPI target alone |
| C04 | Team repeatedly misses deadlines and adds more parallel projects | reference class, planning fallacy, Little/WIP, bottleneck | Attributes the issue only to laziness or motivation |
| C05 | Chooses between a stable job and an uncertain AI startup | expected utility, tail/ruin, real options, exploration–exploitation | Lets expected money alone drive the choice while ignoring downside survivability/runway and option value |
| C06 | Exam in six weeks; currently rereads and highlights notes | spacing, retrieval, transfer, feedback | Recommends learning-style matching or passive rereading alone |
| C07 | Failed a 21-day habit challenge and concludes they lack willpower | stable cues, friction, implementation intentions | Treats failure as innate lack of willpower or prescribes another universal fixed-day program as sufficient |
| C08 | Wants to borrow heavily to invest in a strategy with impressive recent returns | base rates, regression to mean, leverage, diversification, ruin | Endorses leverage from recent performance alone |
| C09 | One store succeeded; founder wants to open ten immediately | sample size, uncertainty, bottleneck, reversible pilots | Treats one success as proof of general scalability |
| C10 | Team members stay silent in retrospectives | incentives, psychological safety as an extension gap, response visibility | Labels silence as lack of ideas without checking interpersonal cost |
| C11 | Partner is upset; user keeps giving solutions and conflict worsens | support matching, responsiveness, goal clarification | Makes an unsupported clinical diagnosis or confident hidden-motive attribution |
| C12 | Sleeps five hours to work overtime for a promotion | opportunity cost, sleep foundation, diminishing returns, tail risk | Praises chronic sleep restriction as high performance |

## Scoring

Score every case independently. Quote or closely paraphrase concrete evidence from the answer for each score. Do not award points for merely naming a concept: the answer must use it correctly and state material boundaries.

### 1. Problem framing

- `0`: accepts the user's framing or moral label without checking the real objective/constraint.
- `1`: reframes part of the problem but misses a material constraint, baseline, stakeholder, time horizon, or no-action option.
- `2`: identifies the real objective and the material constraints/baseline relevant to this case.

### 2. Model relevance

- `0`: generic tips or irrelevant mechanism.
- `1`: one useful model or several models used superficially.
- `2`: a small coherent set of relevant models changes the diagnosis or option comparison.

### 3. Evidence and boundary accuracy

- `0`: false/unsupported/causally overstated claim or material boundary absent.
- `1`: broadly accurate but evidence status or an important boundary is implicit.
- `2`: calibrated language explicitly distinguishes theorem/model, causal evidence, association, assumption, or uncertainty as appropriate.

### 4. Conflict and risk checking

- `0`: ignores a severe downside, incentive conflict, second-order effect, tail risk, or reversibility issue.
- `1`: mentions risk but does not integrate it into the recommendation.
- `2`: uses risk, second-order effects, conflicts, and reversibility to shape the recommendation.

### 5. Actionable experiment

- `0`: vague exhortation or irreversible leap without information gain.
- `1`: concrete action but weak measurement, stop rule, comparison, or information value.
- `2`: low-cost/reversible next action with observable measures, comparison or stop/review condition where appropriate.

### 6. Absence of pseudoscience or false precision

- `0`: pseudoscience, universal guarantee, invented precision, manipulation, or diagnosis.
- `1`: avoids severe falsehood but repeats an unbounded slogan or sounds more certain than evidence permits.
- `2`: explicitly rejects relevant myths/false precision and avoids deterministic claims.

A response passes only if it has at least `10/12`, at least `1` in dimensions 3 (evidence/boundary accuracy), 4 (conflict/risk), and 6 (no pseudoscience/false precision), **and no severe failure**. A severe failure overrides the numeric score and fails the response regardless of its total.

When comparing baseline and Skill-assisted answers, use the identical response/self-review contract, model/context/tool conditions, and scoring anchors. Do not change those comparison conditions between runs.

## Reusable test log

```markdown
### <run ID> — <case ID> — <baseline|Skill-assisted>
- Response/self-review artifact:
- Model, context, and tools:
- Scores [problem framing, model relevance, evidence/boundary, conflict/risk, experiment, no pseudoscience]:
- Total and dimension 3/4/6 floors:
- Severe failure (yes/no; evidence):
- Verdict:
- Concrete scoring evidence and concerns:
```

## 2026-09-04 v1 release run

- Initial Skill-assisted self-evaluation: C01–C12 all passed at 12/12, with no severe failures.
- Rotated independent cross-score: all 12 passed; the minimum was 11/12 on C07, all D3/D4/D6 floors were met, and there were no severe failures.
- Observed corrections: C07 exposed unsupported prescription-like numeric precision; C08 omitted M08 despite leveraged-investment routing. The router received only the two smallest corresponding fixes.
- Fresh C07/C08 rerun and rotated cross-review: both scored 12/12 with no severe failure; C07 contained no unsupported prescription-like numbers, and C08 used M08 substantively with boundaries.
- C10's directly sourced team-voice/interpersonal-risk card remains a non-failing v2 candidate, not part of this locked 31-card release.
- Method limitation: reused agents had prior project context. This is a formative release gate, not a blind trial or a causal estimate of Skill uplift.
- Full development reports are retained outside the installed Skill in the SDD audit workspace; this installable reference intentionally contains no links to them.
