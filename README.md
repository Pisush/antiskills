# antiskills

An anti-skill is a `SKILL.md` file of "do not" rules, written from real bad output that people received. Load it into your agent so it stops producing that output.

## Install

Any agent that reads skills (Claude Code, Codex, Cursor and others):

```
npx skills add Pisush/antiskills
```

Claude Code, as a plugin:

```
claude plugin marketplace add Pisush/antiskills
claude plugin install antiskills@antiskills
```

Or tell your agent: "Install the no-sales-slop skill from https://github.com/Pisush/antiskills".

## Skills

| Skill | Use it when an agent... | Rules | Built from |
|---|---|---|---|
| [no-sales-slop](skills/no-sales-slop/SKILL.md) | writes cold outreach: sales emails, demo requests, partnership offers, beta invitations | 20 | about 35 pitches, Oct to Nov 2026 |

## Share a bad example

Got slop? [Share it in an issue](https://github.com/Pisush/antiskills/issues/new?template=bad-example.yml), with names and other identifying details replaced by placeholders. We turn examples into rules. No sender, company or product is ever named in a skill. Not sure if it counts? [Ask in Discussions](https://github.com/Pisush/antiskills/discussions).

More ways to help are in [CONTRIBUTING.md](CONTRIBUTING.md).

## Why

Building software up to a proof of concept is now cheap. Marketing it is cheap too. So both are on the rise. When the work behind them is not done well, the agent only amplifies the bad work.

Slop is getting easy to spot, and unpleasant to read.

AI skills are on the rise as well. More of them may be AI-generated, and fewer human-curated, than we think.

As a conference organizer I get a lot of sales slop. Some of it asks me to pay. Some of it invites me to be a free tester by "joining an exclusive beta". I want to do my part in improving things.

In software engineering we have patterns, and around them grew anti-patterns. Now we have skills. Here is to the rise of anti-skills.

## How anti-skills are made

Each anti-skill is a short list of rules. The bad examples themselves stay out, so the agent does not learn to copy them. Research on skills found that "do not" rules help agents more than long examples ([Signal or Noise?, 2026](https://arxiv.org/abs/2608.23067)).

## License

MIT. See [LICENSE](LICENSE).
