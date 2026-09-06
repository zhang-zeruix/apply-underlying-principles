# Apply Underlying Principles

[简体中文](README.md) | English

Bring a difficult decision into focus: clarify what matters, examine the mechanisms that might explain it, and identify a next step proportionate to the evidence.

Apply Underlying Principles is a Codex skill containing instructions and reference material: **31 model cards across 4 domains, with 3 modes of use**. It guides an assistant through questions about money, work, learning, relationships, and life choices. It is not a standalone application or a decision engine with demonstrated real-world performance.

The aim is useful depth. A model earns its place in an answer when it changes the diagnosis, comparison of options, or next test. You do not need to know the terminology before asking.

## When it helps

| Domain | Cards and coverage | Example question |
|---|---|---|
| Evidence and systems | 14: base rates, causality, uncertainty, incentives around metrics, feedback, bottlenecks, flow, and reversibility | “We keep missing deadlines. Would starting more projects help?” |
| Money and business | 8: opportunity cost, marginal analysis, specialization, transaction costs, information, incentives, unit economics, and financing | “Customers are growing, but every order loses money. Should we expand?” |
| Work and learning | 5: task switching, retrieval and spacing, learning support, feedback, and habits | “I recognize everything in my notes but cannot explain it without looking.” |
| Social interaction and wellbeing | 4: negotiation, health foundations, relationships and support, autonomy, competence, and connection | “My partner gets more upset when I offer solutions. What should I check?” |

It is particularly useful when several explanations fit the same observation, a local success hides wider costs, or an attractive option carries a downside you cannot afford.

## Quick start

In Codex, ask:

```text
Use $skill-installer to install the skill from
https://github.com/zhang-zeruix/apply-underlying-principles.
Preserve its directory structure and confirm that
$apply-underlying-principles is recognized.
If a skill with that name already exists, report it before replacing anything.
```

Codex supports installing skills from GitHub through `$skill-installer`; newly installed skills are normally detected automatically. Restart Codex if the skill does not appear. See the [official skill guide](https://learn.chatgpt.com/docs/build-skills).

For manual installation, keep the complete skill folder together, including `SKILL.md`, `agents/`, and `references/`. The [official customization guide](https://learn.chatgpt.com/docs/customization/overview) documents these locations:

- Personal: `~/.agents/skills/apply-underlying-principles/`
- Project: `.agents/skills/apply-underlying-principles/`

Then describe your situation in ordinary language, or use this template:

```text
Use $apply-underlying-principles to analyze this decision.

Objective: What I want, and what success would look like.
Facts: What I have actually observed, including the current baseline.
Options: What I could do, including continuing as I am.
Constraints: Time, money, responsibilities, and unacceptable losses.
Uncertainty: What I do not know or may be assuming.

Give a core judgment, explain the relevant models and their limits,
compare the options, and identify what evidence could change the answer.
Suggest a bounded next test if one is appropriate.
```

Incomplete information is normal. The skill directs the assistant to ask when a missing fact could materially change the direction or risk; otherwise, it can proceed with explicit conditions.

## How the reasoning works

1. **Frame the decision.** Establish the objective, observable success, time horizon, people affected, and decision owner.
2. **Find constraints and a baseline.** Examine bottlenecks, incentives, feedback delays, failure costs, comparable situations, and the status quo.
3. **Select 3–7 relevant models.** Read the needed references and explain why each selected model applies, what it predicts, and where it stops applying.
4. **Compare explanations and options.** Check conflicting models, second-order effects, distorted metrics, and tail risks. Include inaction where relevant.
5. **Choose a bounded next step.** When appropriate, design a reversible test with a comparison, one primary measure, a feedback window, and a decision or stop rule.
6. **Revise with evidence.** Separate facts, inferences, and unknowns; state confidence and what would change the conclusion.

Testing is conditional. The workflow does not force an experiment when it would be unsafe, unethical, irreversible, or uninformative. Numerical thresholds and schedules need a user baseline or supporting source; otherwise, they must be identified as provisional hypotheses or examples.

## What intellectual rigor means here

“Underlying principles” are bounded claims, definitions, and models—not permission to treat appealing ideas as universal laws. A valid mathematical derivation does not establish that its assumptions fit your situation. An observed association does not establish that changing one variable will change another.

The [evidence and model-card standard](references/evidence-and-card-standard.md) separates three judgments: strength of evidence, causal interpretation, and suitability for inclusion in the library. These are internal curation rules, not external certification.

| Evidence type | Meaning and permitted interpretation |
|---|---|
| `T` — Theoretical | A mathematical proof, identity, formal derivation, or official definition. Valid under explicit assumptions and correct application; does not establish empirical fit, effect size, or external validity. |
| `A` — Strong empirical support | Consistent high-quality synthesis, preregistered replication, or multiple strong studies without material unresolved contradiction. Supports the bounded claim, without implying large or universal effects. |
| `B` — Credible but bounded empirical support | One high-quality causal study, convergent observational evidence, or a synthesis with material limitations. Use depends on the match between the evidence and the decision. |
| `C` — Preliminary or context-dependent support | Preliminary, indirect, or highly context-dependent evidence, including limited studies or expert interpretation without stronger support. Generates hypotheses only; cannot drive a recommendation without user-specific validation. |
| `X` — Rejected for action | Contradicted, unsupported, unfalsifiable, pseudoscientific, misleadingly generalized, or unacceptably harmful if wrong. May appear only as a warning. |

Causal labels are independently assigned: `causal`, `probable-causal`, `associational`, or `theoretical`. Even strong evidence can be associational. Audit outcomes are also separate: `core` for repeated use within explicit boundaries; `conditional` for use with named conditions or safeguards; `watchlist` for re-review after a stated evidence trigger; and `reject` for exclusion from recommendations.

The assistant should surface competing explanations and evidence against its preferred conclusion. Model count is not a vote: an unacceptable downside can outweigh a higher expected return. Your priorities remain yours: expected money, convenience, fairness, security, and relationships cannot silently substitute for one another.

## A hypothetical example: more closed tickets, more repeat complaints

Suppose a support team reports more closed tickets while repeat complaints also increase. This is an illustration of reasoning, not a report of an observed result.

The first question is whether customers' problems are being resolved. M06, the multitask incentive card, supplies a **theoretical** mechanism: under its assumptions, rewarding a measurable task can divert effort from important tasks that are harder to measure. E07, proxy-metric failure, and S05, local versus overall optimization, are both **`C` hypotheses requiring validation in this team**.

None establishes why complaints rose. Changed reporting definitions, harder cases, or a product defect could explain the pattern. Before changing incentives, inspect a sample of closed and repeat-contact cases, check definitions and case mix, and trace whether premature closure or displaced work actually occurs.

If that local evidence supports the incentive explanation, consider a limited pilot with a comparable group or staged comparison. Make repeat contact about the same issue the primary outcome, with response time and staff workload as guardrails. Choose the observation window and stop rules from the team's baseline and customer feedback delay. An improved pilot metric still needs checks for concurrent changes before a causal conclusion. Broader adoption depends on the result; the example promises no improvement.

## Three modes

| Mode | Example request |
|---|---|
| Application — default | “Use $apply-underlying-principles to compare staying in my job with joining this startup.” |
| Explanation | “Use $apply-underlying-principles to explain opportunity cost: its assumptions, counterexamples, common misuse, and relevance to this choice.” |
| Audit | “Use $apply-underlying-principles to audit this claim: ‘Any metric becomes useless once it is a target.’ Assess its evidence, boundaries, and suitability for the library.” |

Audit checks clarity, evidence, causality, transfer to the intended setting, decision relevance, harm if wrong, and overlap with simpler cards. It returns exactly one curation outcome. It does **not** automatically edit the knowledge base.

## Repository guide

| File | Purpose |
|---|---|
| [README.md](README.md) · [README.en.md](README.en.md) | Chinese and English introductions |
| [SKILL.md](SKILL.md) | Invocation, modes, reference routing, workflow, and guardrails |
| [agents/openai.yaml](agents/openai.yaml) | Display name, default prompt, and invocation policy |
| [evidence-and-card-standard.md](references/evidence-and-card-standard.md) | Evidence definitions, card schema, and audit criteria |
| [epistemics-and-systems.md](references/epistemics-and-systems.md) | 14 evidence, risk, systems, and strategy cards |
| [money-and-business.md](references/money-and-business.md) | 8 money and business cards |
| [work-and-learning.md](references/work-and-learning.md) | 5 work and learning cards |
| [social-and-wellbeing.md](references/social-and-wellbeing.md) | 4 social and wellbeing cards, plus warnings |
| [evaluation-cases.md](references/evaluation-cases.md) | 12 formative cases, scoring rules, and release-run notes |

## Validation and limitations

The twelve evaluation cases test framing, model use, evidence boundaries, risks, next steps, and avoidance of pseudoscience or false precision. Release notes record corrections and subsequent reviews. Reused agents had prior project context: these checks were not blinded and provide no independent proof of real-world decision uplift.

Core reference material is mainly Chinese. Cards record a source review date of **2026-09-04**; this static collection does not update automatically. Changing or high-stakes medical, legal, financial, and safety claims require current authoritative sources at decision time. The skill offers no outcome guarantees or medical or psychological diagnosis and does not replace relevant professional judgment.

Instructions do not guarantee correct execution or answers: results depend on the host model, input quality, and available tools. Feedback does not automatically update the knowledge base; revisions require an explicit decision and review.

## Contributing

Propose an exact, bounded claim with directly supporting evidence, assumptions, counterexamples, and the decision it could change. Include a real anonymized case when available, clearly separated from hypothetical illustrations. Explain uncertainty and harm if wrong. Contributions require review under the card standard; suggestions and anecdotes are not automatically ingested into the library.
