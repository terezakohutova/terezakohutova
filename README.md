### Marketing & Partnerships, run on AI agents I build myself

I work in e-commerce and fintech marketing across CZ/SK/PL/DE, and I build
the AI agents that do the operational work myself, not just prompt someone
else's. One marketer, four markets: a five-language website shipped in a
month, paid ads in four countries, 100+ lifecycle e-mails in four languages.
The agents draft and check. I decide and publish.

**Step zero is always a person.** An agent can set up an account, write the
copy and check it, but it can't decide what the goal is, what it may cost or
whether a sentence is true. So every repo here follows one rule: the agent
drafts and stages, a person publishes. No agent is handed a posting
credential, a payment method or a live-launch switch; agents that run on a
schedule only read and report; every live change is written down first with
the old value and a way back. Every repo has tests and CI, and every claim in
a README points to something you can run.

- **[paid-ads-agent-playbook](https://github.com/terezakohutova/paid-ads-agent-playbook)**: Claude Code subagents for Google Ads and Meta Ads, audit through launch, blind-scored on a sample client, plus the ops layer that keeps them honest over time: weekly checks, a goals check-in so they ask instead of guess, a change ledger with rollback and a spelling and grammar gate for ad copy.
- **[claude-code-architecture-showcase](https://github.com/terezakohutova/claude-code-architecture-showcase)**: the workspace architecture behind it (CLAUDE.md index, one rule per file, hooks, skills, scoped agents), including the hooks that turn a repeatedly broken rule into a hard gate.
- **[ai-marketing-playbook](https://github.com/terezakohutova/ai-marketing-playbook)**: patterns for marketing and e-commerce ops (inventory sync, a partner CRM steward, staged outreach, safe scheduled agents). Two come with a runnable agent, hand-written answer keys and a scorer.
- **[website-builder-agent](https://github.com/terezakohutova/website-builder-agent)**: an agent and skill that build a multi-language marketing website from brief to go-live: build pipeline, translations, SEO and AI-search visibility, consent, QA across devices and in-app browsers. Ships with a sample site and its real QA report.
- **[copy-langcheck](https://github.com/terezakohutova/copy-langcheck)**: a spelling and grammar gate for marketing copy in Czech, Slovak, Polish, German and English (Hunspell + LanguageTool) that fails the build on a mistake, and fails loudly when it could not check at all.

And one for the people at the desk:

- **[kocicka](https://github.com/terezakohutova/kocicka)**: a desktop cat in a wheelchair who counts your real working time and makes you take a guided break every hour. One Python file, no dependencies, nothing leaves your machine.

#### Every mistake became a rule

Most of what these repos enforce started as something that went wrong once.

| What happened | The rule since |
|---|---|
| Two of ten agents in a batch reported "done" and weren't | Check the result, not the report |
| An e-mail passed every test and was unreadable in Gmail dark mode on an iPhone | Test on a real phone before it ships |
| Campaigns chased installs instead of people who actually use the product | Give the agent the exact goal, as one number |
| An agent invented customer reviews for a landing page | Facts come from a person or a source, never from the model |
| An amount in euros was carried over as the same number in another currency | Currencies and amounts are checked by a script |
| An agent published a draft without asking | Only a person publishes or sends |

The fix is never a cleverer prompt. It's written context: one rule per file,
read before every task, and a hook once a rule keeps getting broken.
