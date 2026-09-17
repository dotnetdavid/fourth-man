---
name: fourth-man
description: Use for structured dissent on consequential claims.
version: 0.1.0
author: David Frey, Hermes Agent
license: MIT
platforms: [windows, linux, macos]
metadata:
  hermes:
    tags: [critical-thinking, structured-dissent, red-team, reasoning, decision-support]
    related_skills: [socratic-decision-support, grounded-citations, aegis]
---

# Fourth Man

Use structured dissent to test a consequential claim when apparent agreement may conceal a shared assumption. The method broadens analysis, constructs the strongest credible countercase, preserves the debate trail, and organizes evidence for a human decision. It does not establish truth, diagnose a person, prescribe treatment, or grant decision authority to an agent.

## When to Use

Use this skill when a decision is consequential, ambiguous, costly to reverse, or rests on a load-bearing assumption, including:

- software architecture, implementation, risk, and policy decisions;
- research claims, plans, and evidence syntheses;
- strategic, organizational, or personal planning questions;
- philosophical questions that benefit from premise analysis and strong counterarguments;
- educational or hypothetical medical evidence-appraisal exercises with appropriate safety limits.

Do not use it for simple, reversible questions, routine factual lookups, or when a direct answer is sufficient. Do not use it to generate patient-specific diagnosis, treatment, medication, triage, or emergency advice; route those situations to qualified clinical care or emergency services as appropriate.

## Core Principles

1. **Consensus is a challenge trigger, not proof.** Three similar answers may reflect shared evidence, framing, or model failure.
2. **Require a countercase, not a false assertion.** The fourth analyst must build the strongest evidence-grounded contrary case and may report `no material objection found`.
3. **Freeze starting positions.** Publish initial analyses and the countercase before debate. Never rewrite the original record.
4. **Debate evidence, not personalities.** Every response identifies the claim, evidence, position change, reason, and remaining uncertainty.
5. **Resolve what can be checked.** Use tests, source checks, calculations, schemas, experiments, or other deterministic validation where appropriate.
6. **Preserve unresolved dissent.** A majority response cannot erase a concern that lacks a decisive evidentiary answer.
7. **Keep a human accountable.** Agents organize analysis; the designated human owns the final disposition.

## Procedure

### 1. Establish the decision packet

State the decision boundary before generating analysis:

```text
Decision or claim:
Why it matters:
Consequences if wrong:
Known constraints and non-goals:
Evidence boundary and source authority:
Validation evidence available:
Human decision owner:
```

Classify the question as factual, empirical, practical, philosophical, or mixed. State whether the purpose is to decide, learn, test a hypothesis, or discover what remains unknown. Do not begin a four-agent process until this packet is concrete.

### 2. Run three independent first passes

Keep the analyses blind until all are complete. Assign distinct lenses:

| Analyst | Required emphasis |
|---|---|
| A — primary path | Simplest credible conclusion, expected outcome, assumptions, and supporting evidence |
| B — risk path | Failure modes, unintended consequences, safety concerns, counterevidence, and dependency risks |
| C — alternatives path | Competing explanations, boundary cases, opportunity costs, and credible alternatives |

Each analyst must record:

```text
Conclusion or recommendation:
Material assumptions:
Evidence with provenance:
Counterevidence considered:
Unknowns and limitations:
What would change the conclusion:
```

Role variation is not proof of independence. When proportionate to the risk, diversify evidence paths, tools, or model families and state any remaining correlation limits.

### 3. Determine whether structured dissent is warranted

Trigger the fourth analyst only when both conditions hold:

1. The decision is consequential, ambiguous, or costly to reverse.
2. The three first passes converge on a material conclusion or load-bearing assumption.

Do not manufacture a fourth position when the first analyses already reveal meaningful disagreement, an outlier concern, or insufficient evidence. Preserve those signals for the decision owner.

### 4. Construct the fourth-seat countercase

Give the fourth analyst the anonymized decision packet, frozen analyses, sources, and stated unknowns. Do not provide agent identities, conversational persuasion, or a requested outcome.

Use this instruction:

> Assume the apparent consensus may contain a material blind spot. Build the strongest credible countercase that the evidence permits. Do not invent facts, treat unanswered questions as disproof, or manufacture disagreement for its own sake.

Require this output:

```text
Countercase thesis:
Consensus claim and shared assumption challenged:
Evidence supporting the countercase:
Evidence that weakens the countercase:
Missing evidence or unresolved uncertainty:
Falsifying check, experiment, calculation, or source:
Consequence if the countercase is true:
Recommended disposition: revise, mitigate, investigate, accept explicit risk, defer, or no material objection found:
```

### 5. Publish the trail and run a bounded debate

Publish the immutable three first passes and countercase before interaction begins. Then run a bounded, evidence-focused debate. Each reply must contain:

```text
Claim addressed:
Evidence or source relied upon:
Position: changed, narrowed, or unchanged:
Reason for that position:
Remaining uncertainty:
```

Use the smallest number of rounds that resolves the material issue. If no limit is specified, permit one response to each material counterclaim and one final synthesis. A human may authorize another round only when new evidence or a newly defined test would change the decision.

Each final analyst position must link to its starting position. The record must show where each analyst began, how it reacted to dissent, what evidence changed its view, and which concerns remain unresolved.

### 6. Validate and classify the countercase

Classify every material counterclaim as:

| Disposition | Meaning |
|---|---|
| Accepted | It changes the conclusion or reveals a missing requirement. |
| Partially accepted | It changes a risk, limitation, mitigation, or validation need. |
| Rebutted with evidence | Inspectable evidence weakens the countercase. |
| Unresolved | More validation, explicit risk acceptance, deferral, or escalation is required. |

Never settle the result by vote, confidence language, or rhetorical dominance. Treat a source first introduced by an analyst or countercase as an unverified lead until it is independently retrieved, checked for scope and support, registered through `grounded-citations`, and distinguished from the analyst’s interpretation.

### 7. Produce the human decision brief

```text
Initial consensus:
Countercase:
Evidence for and against:
Shared assumptions tested:
Evidence discovered during debate:
What changed and why:
What survived challenge:
Unresolved uncertainty:
Validation or escalation trigger:
Human decision and rationale:
```

Stop at the stated decision boundary. If no accountable human decision owner exists for a consequential result, state that authority is unresolved and do not imply approval.

## Domain Adapters

### Programming and systems

Treat executable tests, reproductions, contracts, schemas, static checks, and observable runtime behavior as the strongest evidence. The countercase should identify a concrete failure path, test gap, compatibility conflict, or unstated requirement. A passing agent debate never substitutes for a failing or missing test.

### Research and evidence claims

Use `web_search`, `web_extract`, and `grounded-citations` for external claims. Separate primary evidence, secondary interpretation, inference, and unknowns. The countercase should seek disconfirming evidence, alternative causal explanations, source-quality limitations, and missing measurements.

### Medical or health-related exercises

Use this skill only for educational, hypothetical, or public evidence-appraisal scenarios—not individual medical care.

- Do not diagnose, prescribe, recommend medication changes, estimate personal risk, or direct a person’s care.
- Use current authoritative sources such as professional guidelines, public-health authorities, or peer-reviewed evidence; cite them precisely.
- Make uncertainty, evidence limits, and the need for qualified clinical judgment explicit.
- Treat safety flags as reasons to stop the exercise and recommend appropriate professional or emergency evaluation, not as material for agent debate.
- Evaluate the skill on source quality, uncertainty handling, counterevidence, and safe escalation—not on whether it chooses a patient action.

### Philosophy and ethics

State the question, the terms in dispute, and the evaluation standard before judging arguments. Distinguish logical validity, empirical premise support, interpretive disagreement, and value conflict. The countercase should steelman a credible opposing view. Do not claim that a debate has resolved a normative question when disagreement rests on unshared values.

## Evaluation and Testing

Test the skill across domains using a held-out scenario set. Compare a normal single-pass or ordinary review against the Fourth Man process.

### Programming cases

Use problems with runnable tests, known bugs, compatibility constraints, or reproducible failures. Score whether the countercase identifies a real missing check, assumption, defect, or safer alternative that ordinary review missed.

### Medical evidence-appraisal cases

Use public, synthetic, or retrospective cases with source-grounded answer keys and qualified review where possible. Score citation quality, separation of evidence from inference, recognition of uncertainty, and safe refusal to make patient-specific decisions. Do not use personal health records or real-time treatment choices as test material.

### Philosophy cases

Use questions with named premises, competing frameworks, or known objections. Score premise clarity, fair steelmanning, detection of equivocation or hidden value assumptions, and honest preservation of unresolved disagreement. Do not score a single “correct” answer where the task is genuinely normative.

### Cross-domain measures

Measure:

- distinct decision-relevant assumptions surfaced;
- useful counterevidence or falsifying checks found;
- corrections or mitigations adopted;
- unsupported claims or invented sources detected;
- countercases rebutted by evidence rather than votes;
- unresolved concerns preserved;
- false or low-value objections;
- added time, cost, and cognitive burden;
- confusion about authority or unsafe domain behavior.

## Pitfalls

- Do not treat multiple outputs from the same model, prompt, or evidence packet as independent evidence.
- Do not force a claim of error when the countercase has no material support.
- Do not permit open-ended debate; it creates conformity and rhetoric without necessarily increasing evidence.
- Do not overwrite initial positions after a debate; loss of provenance makes conformity indistinguishable from learning.
- Do not let agents vote, approve, or close an accountable human decision.
- Do not use hypothetical medical testing as a route around medical safety, professional judgment, or evidence standards.
- Do not let philosophical disagreement be mislabeled as factual uncertainty or vice versa.
- Do not claim the method discovers truth. It improves the inspection of reasoning and evidence.

## Verification

A completed Fourth Man cycle is valid only when all of the following are present:

- a concrete decision packet and designated human decision owner;
- three frozen first-pass analyses with declared assumptions, evidence, and limits;
- a fourth-seat countercase or a documented reason the trigger did not apply;
- a preserved debate trail linking final positions to their starting positions;
- claim-level dispositions supported by appropriate evidence or explicit uncertainty;
- deterministic validation for checkable material claims;
- a final human decision brief that preserves unresolved dissent;
- for medical exercises, source-grounded educational scope and no patient-specific recommendation.
