# Fourth Man

When everyone agrees on an important decision, it can be easy to miss the same bad assumption together. Fourth Man gives that decision a fair second look.

It starts with a few independent first takes. Then a fourth analyst makes the strongest honest case for why the group might be wrong. The goal is not to manufacture conflict. Sometimes the right result is "no material objection found."

A person still owns the decision. Fourth Man helps people inspect the reasoning and evidence before they make it.

## A simple use case

A team wants to cache authorization decisions for 15 minutes to make an application feel faster. Three initial reviews agree that the change looks safe.

Fourth Man asks a different question: what happens when a person's access is revoked, their role changes, or an administrator disables their account? It suggests a check: revoke access and confirm that every request is denied quickly enough, even while a cached decision exists.

The team may still use the cache. Or it may shorten the cache, add invalidation, or decide the risk is not worth it. The human decision owner chooses. Fourth Man makes sure the shared assumption got a real test before that choice.

## When it helps

Use it for decisions that matter, are unclear, or would be costly to undo: a system design, a research claim, a policy choice, or a plan with a big assumption underneath it.

Skip it for small, routine questions where a direct answer is enough.

## What it does not do

Fourth Man is not a vote, approval gate, or substitute for human judgment. A group of similar answers is not proof, and a clever counterargument is not proof either. The method keeps the question, evidence, and remaining uncertainty visible so the decision owner can make an informed call.

For health-related topics, it supports public evidence appraisal and educational discussion only. It does not diagnose a person or recommend treatment, medication, triage, or emergency action.

## Install in Hermes

Put this folder in your active Hermes profile's `skills` directory, keeping the skill at `fourth-man/SKILL.md`. Start a new Hermes session, then ask for Fourth Man when you want a structured challenge to an important decision.

## About this repository

This repository holds the reusable skill. Private experiments, project records, and evaluator material stay in their own private workspaces.

## License

MIT. See [LICENSE](LICENSE).
