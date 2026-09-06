# Evidence and model-card standard

This is the normative contract for every domain model card and its audit. Evidence strength, causal interpretation, and curation status are separate judgments; never infer one from another.

## Evidence types

| Type | Meaning | Minimum interpretation |
|---|---|---|
| `T` | Theoretical: a mathematical proof, identity, formal derivation, or official definition. | Valid only conditional on explicit assumptions and correct application; it does not establish empirical fit, effect size, or external validity. |
| `A` | Strong empirical support: consistent high-quality synthesis, preregistered replication, or multiple strong studies with no material unresolved contradiction. | High confidence in the stated, bounded claim. It does not imply a large effect, no heterogeneity, or universal applicability. |
| `B` | Credible but bounded empirical support: one high-quality causal study, convergent observational evidence, or a synthesis with material limitations. | Useful when its population, intervention/exposure, comparator, outcome, and horizon match the decision; retain explicit uncertainty. |
| `C` | Preliminary, indirect, or highly context-dependent support, such as a single limited study or expert interpretation not backed by stronger evidence. | Hypothesis-generating only. It may not drive a recommendation without user-specific validation. |
| `X` | Rejected for action: contradicted, unsupported, unfalsifiable, pseudoscientific, misleadingly generalized, or unacceptably harmful if wrong. | May appear only as a warning, never as support for a recommendation. |

`A` does **not** mean the effect is large or universal. `T` does **not** mean its assumptions hold in the user's setting. Do not upgrade a type because a mechanism sounds plausible, a source is famous, or a result is convenient.

## Causal labels

Use exactly one label for the card's accurate statement:

- `causal`: credible identification supports that changing the stated cause changes the outcome in the stated population and conditions. Name the design and material assumptions.
- `probable-causal`: triangulated evidence and mechanism make causation more likely than the main alternatives, but residual confounding, transport, or design uncertainty remains. Use probabilistic language.
- `associational`: evidence establishes covariation or prediction only. Do not convert it into intervention advice without an additional causal argument or user-specific test.
- `theoretical`: the statement follows from a definition or model under assumptions; empirical applicability has not been established by that derivation.

Evidence type and causal label are orthogonal. An `A` synthesis can still be `associational`; a well-identified but narrow study can be `B; causal`. A `T` card should normally be `theoretical`. When one sentence mixes theoretical and empirical claims, split it into separate cards or narrow the accurate statement.

## Source hierarchy and review

Prefer sources in this order, while checking their fitness for the exact claim:

1. mathematical proof or official definition;
2. current authoritative guideline;
3. preregistered replication;
4. systematic review or meta-analysis;
5. high-quality causal study;
6. convergent observational evidence;
7. single study;
8. expert interpretation;
9. anecdote.

Position in the hierarchy does not automatically set `T`/`A`/`B`/`C`/`X`. Before assigning a type or writing the accurate statement, inspect:

- effect size and practical importance;
- uncertainty, including intervals and sensitivity analyses;
- heterogeneity across studies or subgroups;
- population and setting;
- intervention or exposure and comparator;
- measured outcome rather than a proxy;
- time horizon and feedback delay;
- publication and selective-reporting bias;
- conflicts of interest and funding;
- publication, update, and access date.

Use a directly supporting source, not a search result, tertiary summary, or citation that merely mentions the topic. Note material disagreement rather than averaging it away. Anecdote may suggest a diagnostic question, but it cannot establish a general effect.

For dynamic claims and high-stakes claims, browse at decision time and link current authoritative sources. This includes claims materially affected by current law, regulation, prices, product terms, clinical or safety guidance, financial conditions, or other changing external state. Prefer primary official sources and record the review date. If current evidence or a required source is unavailable, lower the evidence type and confidence, narrow or defer the recommendation, or omit the card; never fill the gap with intuition.

## Required model-card schema

Every card must use this exact heading, field labels, and field order:

```markdown
## <ID> — <Chinese name>

- **Accurate statement:**
- **Evidence:** <T|A|B|C|X>; <causal label>; reviewed 2026-09-04
- **Mechanism or derivation:**
- **Use when:**
- **Do not use when:**
- **Diagnostic questions:**
- **Actions:**
- **Common misuse:**
- **Interactions:**
- **Sources:**
```

Field requirements:

- **Accurate statement:** State the smallest defensible claim. Include material conditions; avoid slogans and deterministic promises.
- **Evidence:** Use one evidence type and one causal label defined above. The review date records when source currency was last checked, not when the idea was first published.
- **Mechanism or derivation:** Explain the link from inputs to outcomes and identify assumptions. Do not use a plausible story as proof.
- **Use when:** Give observable conditions that make the card decision-relevant.
- **Do not use when:** State counterconditions, scope limits, contraindications, and important alternative explanations.
- **Diagnostic questions:** Ask only questions that can change model selection, confidence, risk, or action.
- **Actions:** Prefer a low-cost, reversible next step with a baseline or comparison, primary measure, feedback window, and decision/stop rule when applicable.
- **Common misuse:** Name the tempting overgeneralization, causal leap, metric gaming, or false precision this card must prevent.
- **Interactions:** Identify cards that complement, conflict with, dominate, or set a prerequisite for this card.
- **Sources:** For empirical cards, include at least one directly supporting authoritative source. For theoretical cards, include the defining proof or primary source. Link each source directly and make clear which part of the statement it supports.

`C` cards may not drive a recommendation without user-specific validation. `X` cards may appear only as warnings. If a card cannot meet its source requirement, it is incomplete. A source-incomplete empirical candidate may only be `watchlist` with a named evidence trigger or `reject`; it cannot be `core` or `conditional` and may not drive a recommendation.

## Curation decision rule

Audit each candidate separately on all seven criteria; record `pass`, `concern`, or `fail` plus a one-sentence reason for each:

1. **Clarity:** Is the statement precise, falsifiable where applicable, and free of slogan-like ambiguity?
2. **Evidence strength:** Do source quality, consistency, effect size, uncertainty, and bias justify the evidence type?
3. **Causal validity:** Does the causal label match the design and assumptions, without converting association into intervention effect?
4. **External validity:** Do population, setting, comparator, outcome, and time horizon transfer to the intended use?
5. **Decision relevance:** Can the card change a diagnosis, option comparison, risk check, or next test?
6. **Harm if wrong:** Are downside, irreversibility, tail risk, and safeguards proportionate to uncertainty?
7. **Simpler coverage:** Does an existing simpler card already explain the same decision-relevant mechanism?

Assign exactly one outcome after the seven judgments:

- `core`: clear, decision-relevant, non-duplicative, and supported strongly enough for repeated use within explicit boundaries; harm controls are adequate.
- `conditional`: useful only under named conditions, with bounded evidence or transfer; the card must state the validation or safeguard required before action.
- `watchlist`: plausible or emerging, but presently too uncertain, indirect, redundant, or unstable to guide a recommendation; retain only for re-review with a stated evidence trigger.
- `reject`: false, unfalsifiable, materially misleading, needlessly duplicative, or too dangerous relative to support; exclude from recommendations. An `X` warning records why it was rejected.

Choose the most conservative outcome required by any material failure. Popularity, intuitive appeal, and ease of explanation are not curation criteria.
