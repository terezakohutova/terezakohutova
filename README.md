### Marketing and partnerships, with AI agents I build myself

I'm the only marketer for e-commerce and fintech brands in Czechia, Slovakia,
Poland and Germany. Most of the routine work, such as audits, translations and
checks, runs through Claude Code agents I wrote. I decide what goes out: none of
the agents can post, pay or launch anything.

<a href="https://www.linkedin.com/in/terezakohutova/"><img src="https://img.shields.io/badge/LinkedIn-0A66C2?logo=linkedin&logoColor=white&style=flat" alt="LinkedIn" /></a>

#### Currently

- Publishing small, single-purpose tools from my own workspace: one script, hook or skill at a time
- Running marketing audits from the outside with a team of agents, every fact checked before it goes in a report
- Every repo below has tests and CI

#### Repos

- **[paid-ads-agent-playbook](https://github.com/terezakohutova/paid-ads-agent-playbook)**: Google Ads and Meta Ads audit agents. A fresh agent found 16 of 18 planted problems on Google and 12 of 12 on Meta.
- **[claude-code-architecture-showcase](https://github.com/terezakohutova/claude-code-architecture-showcase)**: my Claude Code workspace with the company taken out: one rule per file, skills, scoped agents, five hooks with 133 tests.
- **[ai-marketing-playbook](https://github.com/terezakohutova/ai-marketing-playbook)**: five patterns for marketing operations; two ship as agents scored against answer keys.
- **[website-builder-agent](https://github.com/terezakohutova/website-builder-agent)**: build a multi-language marketing site, written down from a real build.
- **[copy-langcheck](https://github.com/terezakohutova/copy-langcheck)**: spelling and grammar gate for copy in CZ, SK, PL, DE and EN that also fails when it could not check.
- **[rodopis-genealogy-agents](https://github.com/terezakohutova/rodopis-genealogy-agents)**: 14 agents that research a family tree, every fact cited, deceased ancestors only.
- **[claude-code-token-audit](https://github.com/terezakohutova/claude-code-token-audit)**: finds which subagents waste tokens and why. One offline Python script.
- **[kocicka](https://github.com/terezakohutova/kocicka)**: a desktop cat in a wheelchair who sends you on a break every hour. One Python file, nothing leaves your computer.

#### Where the rules came from

| What went wrong | Rule since then |
|---|---|
| Two of ten agents in a batch reported "done" and weren't | Check the result, not the report |
| An e-mail passed every test and was unreadable in Gmail dark mode on an iPhone | Test on a real phone before it ships |
| An agent invented customer reviews for a landing page | Facts come from a person or a source |
| An agent published a draft without asking | Only a person publishes or sends |

Each rule is a short file the agents read before every task. When a rule keeps
getting broken anyway, it becomes a hook that blocks the action.
