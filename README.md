### Marketing & Partnerships, run on AI agents I build myself

I work in e-commerce and fintech marketing across CZ/SK/PL/DE, and I build
the AI agents that do the operational work myself, not just prompt someone
else's.

Every repo here has tests and CI, and every claim in a README points to
something you can run or read in the repo. They all follow one rule: the
agent drafts and stages, a person publishes. No agent is handed a posting
credential, a payment method or a live-launch switch; agents that run on a
schedule only read and report; every live change is written down first
with the old value and a way back.

- **[paid-ads-agent-playbook](https://github.com/terezakohutova/paid-ads-agent-playbook)**: runnable Claude Code subagents for Google Ads and Meta Ads, audit through launch, plus the ops layer that keeps them honest over time: a cadence of weekly checks and monthly audits, a goals check-in so they ask instead of guess, a change ledger with rollback, automatic file versions and a multilingual spelling and grammar gate for ad copy. Ships with a sample client and a verified audit run.
- **[claude-code-architecture-showcase](https://github.com/terezakohutova/claude-code-architecture-showcase)**: the workspace architecture (CLAUDE.md index, feedback rules, hooks, skills, scoped agents) behind the automation I actually run, including the hooks that turn a repeatedly broken rule into a hard gate and keep a version of every rule before it is edited.
- **[ai-marketing-playbook](https://github.com/terezakohutova/ai-marketing-playbook)**: reusable patterns for marketing and e-commerce ops (listing generation, cross-platform inventory sync, staged outreach, a partner CRM steward, safe scheduled agents), generalized from production. Two of them come with a runnable agent and a blind-tested sample run.
- **[website-builder-agent](https://github.com/terezakohutova/website-builder-agent)**: a Claude Code agent and skill that build a multi-language marketing website from brief to go-live: build pipeline, design system, translations, SEO and GEO, consent and legal pages, QA across devices, widths and in-app browsers, and backups at every step. Distilled from a five-language site I shipped and hardened; ships with a sample site and its real QA report.
- **[copy-langcheck](https://github.com/terezakohutova/copy-langcheck)**: a spelling and grammar gate for marketing copy in Czech, Slovak, Polish, German and English (Hunspell + LanguageTool, Korektor optional), one Python file that fails the build when the copy has a mistake, and fails loudly when it could not check at all.

And one for the people at the desk:

- **[kocicka](https://github.com/terezakohutova/kocicka)**: a desktop cat in a wheelchair who counts your real working time and makes you take a guided break every hour. One Python file, no dependencies, nothing leaves your machine.
