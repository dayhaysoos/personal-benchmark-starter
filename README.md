# Personal Benchmark Starter

Use this template to create a personal LLM benchmark repo.

The methodology lives in [dayhaysoos/personal-benchmark-framework](https://github.com/dayhaysoos/personal-benchmark-framework). This starter gives you the downstream repo shape so you can begin filling in your own benchmark.

## Create A Benchmark Repo

With GitHub CLI:

```bash
gh repo create my-benchmark --template dayhaysoos/personal-benchmark-starter --public --clone
```

Then open the new repo and paste this into your agent:

```text
Use this repository as a downstream personal LLM benchmark repo.

Use https://github.com/dayhaysoos/personal-benchmark-framework as the methodology source. Follow its agent playbooks conceptually.

Interview me one question at a time. I am the benchmark author.

Do not invent my benchmark lens, policies, scenario judgments, candidate annotations, scores, or report claims. If any judgment is unclear, ask me.

When I give you a benchmark name or topic, propose a short starter draft and ask me to accept or edit it instead of asking me to fill a blank template.

Start by helping me define:
1. what model behavior this personal benchmark should examine,
2. what the benchmark does not test,
3. the first 1-3 policies,
4. the first 3-5 smoke scenarios.

V1 benchmarks LLM responses only. Agents are helpers, not benchmark targets.
```

This starter also includes [AGENTS.md](AGENTS.md) with repo-local agent instructions. If your agent automatically reads that file, you can start with a shorter message:

```text
My benchmark is called my-benchmark. It should examine LLM behavior on [topic].
```

The same prompt also lives in [AGENT_PROMPT.md](AGENT_PROMPT.md).

The first interaction should be low-friction: after you provide a benchmark name or topic, the agent should propose a starter lens for you to accept or edit.

That starter lens should include both choosing behavior and rejection behavior: the model should choose from supplied facts/candidate action IDs/policies while rejecting invalid options, plausible traps, and unsupported assumptions.

## Repo Structure

- [eval-card.md](eval-card.md): what this benchmark tests and does not test.
- [glossary.md](glossary.md): terms used by scenarios.
- [policies.md](policies.md): behavior policies used in scenarios.
- [rubric.md](rubric.md): scoring rules.
- [model-prompt.md](model-prompt.md): default prompt shape for LLM runs.
- [scenarios/](scenarios): Markdown scenarios with prompt-facing data and author annotations.
- [runs/](runs): run manifests, raw outputs, and scores.
- [reports/](reports): static HTML reports.

## First Milestone

Do not start with a full benchmark. Start with a smoke set:

1. Define the benchmark lens in `eval-card.md`.
2. Define 1-3 policies in `policies.md`.
3. Create 3-5 scenarios in `scenarios/`.
4. Run one model with deterministic settings.
5. Confirm scores as the benchmark author.
6. Generate one HTML report.

## Claim Boundary

This template is for personal benchmarks. Your benchmark reflects your judgment standard. It should not claim universal consensus unless you intentionally build that process yourself.
