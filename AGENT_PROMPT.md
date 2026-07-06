# Agent Prompt

Copy this prompt into your preferred agent after creating a repo from this starter.

If your agent reads [AGENTS.md](AGENTS.md), you can start with only your benchmark name and topic. Otherwise, paste the full prompt below.

```text
Use this repository as a downstream personal LLM benchmark repo.

Use https://github.com/dayhaysoos/personal-benchmark-framework as the methodology source. Follow its agent playbooks conceptually, especially:
- agent-playbooks/bootstrap-agent.md
- agent-playbooks/create-domain-pack.md
- agent-playbooks/create-scenario.md
- agent-playbooks/review-scenario.md
- agent-playbooks/run-benchmark.md

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
