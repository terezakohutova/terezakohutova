### Marketing and partnerships, with AI agents I build myself

I work in e-commerce and fintech marketing in Czechia, Slovakia, Poland and
Germany. Being the only marketer for these markets has meant a website in five
languages shipped in a month, paid ads in each country and over 100 lifecycle
e-mails. Much of the routine work, such as audits and translations, runs
through Claude Code agents I wrote.

I decide what goes out, so none of the agents has a posting login, a payment
method or a launch button. The ones that run on a schedule only read and
report. Before any live change, the old value goes into a log so the change can
be undone. Every repo below has tests and CI.

- **[paid-ads-agent-playbook](https://github.com/terezakohutova/paid-ads-agent-playbook)**: two agents that audit Google Ads and Meta Ads accounts by a fixed checklist. On a fictional account with planted problems, a fresh agent that never saw the answer key found 16 of 18 on Google and 12 of 12 on Meta. The repo also has weekly checks, a change log with rollback and a spelling check for ads.
- **[claude-code-architecture-showcase](https://github.com/terezakohutova/claude-code-architecture-showcase)**: how my Claude Code workspace is organised, with the company taken out: one rule per file, skills, scoped agents and five hooks with 133 tests.
- **[ai-marketing-playbook](https://github.com/terezakohutova/ai-marketing-playbook)**: five patterns for marketing operations, such as keeping stock in sync across marketplaces or cleaning up a partner CRM. Two come with a working agent, hand-written answer keys and a scorer.
- **[website-builder-agent](https://github.com/terezakohutova/website-builder-agent)**: an agent and skill for building a multi-language marketing site, written down from a real build, with a sample site and its QA report.
- **[copy-langcheck](https://github.com/terezakohutova/copy-langcheck)**: spelling and grammar check for marketing copy in Czech, Slovak, Polish, German and English (Hunspell and LanguageTool). It fails the build on a mistake, and also when it could not check the text at all.
- **[rodopis-genealogy-agents](https://github.com/terezakohutova/rodopis-genealogy-agents)**: 14 agents that research a family tree one person at a time. Facts are checked against the original record and cited, and it only works on deceased ancestors.
- **[kocicka](https://github.com/terezakohutova/kocicka)**: a desktop cat in a wheelchair who counts your real working time and sends you on a guided break every hour. It is a single Python file with no dependencies, and nothing leaves your computer.

Most of the agents have the persona of a historical figure who did similar
work: Edison runs the Google Ads audit, Barnum the Meta one, and a Czech
genealogist leads the family tree research. The persona only changes how the
agent talks in chat; what it writes to files is neutral.

#### Where the rules came from

| What went wrong | Rule since then |
|---|---|
| Two of ten agents in a batch reported "done" and weren't | Check the result, not the report |
| An e-mail passed every test and was unreadable in Gmail dark mode on an iPhone | Test on a real phone before it ships |
| Campaigns chased installs instead of people who use the product | Give the agent the exact goal, as one number |
| An agent invented customer reviews for a landing page | Facts come from a person or a source |
| An amount in euros was carried over as the same number in another currency | A script checks currencies and amounts |
| An agent published a draft without asking | Only a person publishes or sends |

Each rule is a short file the agents read before every task. If a rule keeps
getting broken anyway, I turn it into a hook that blocks the action.
