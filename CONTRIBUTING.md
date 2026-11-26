# Contributing

Anti-skills only work if they come from real bad output that a person actually saw. Contributions are welcome. The easiest one takes two minutes.

## Share a bad example (easiest)

Open an issue with the **Share a bad example** form and paste the slop you received. Replace names, emails, phone numbers, company and product names, links and addresses with placeholders like [NAME] or [COMPANY]. Issues are public, so please check twice. Quote only what shows the pattern. If personal data slips through, we delete the whole issue, see [SECURITY.md](SECURITY.md). We turn the examples into rules. The examples themselves never go into a skill. Tick the box in the form if you want your GitHub handle credited in the skill.

What happens next: a maintainer reads the issue and adds the label `turn-into-rules`. An agent then drafts new or updated rules and opens a pull request. A maintainer reviews it before anything is merged.

## Add a rule to an existing anti-skill

1. Open an issue or a pull request against the skill's `SKILL.md`.
2. Write the rule as one line that says what not to do, then one short sentence on why it fails.
3. Say where the pattern came from, in general terms. For example, "three cold emails to an open source maintainer in 2026". Do not name the sender.

## Add a new anti-skill

1. Copy `template/SKILL.md` into a new folder `skills/<name>/`. Use lowercase letters and hyphens for the name.
2. Fill in the two required fields at the top:

   ```yaml
   ---
   name: <name>
   description: <what it prevents, and when an agent should use it>
   ---
   ```

3. Write rules, not examples. A list of "do not" lines works better than pasted bad output, and the agent will not learn to copy it.
4. Keep it short. Under 100 lines is a good target.
5. End with a short check the agent can run before it is done.
6. Add a row for it to the table in the README.
7. Open a pull request. The template asks where the patterns come from and how you tested it. No issue is needed first.

## Rules for every contribution

- **Base it on things you received or reviewed yourself.** You may use AI to help with the wording, but you must have seen each pattern with your own eyes. That is the point of this repo.
- **Skills contain rules, not examples.** Anonymized examples belong in issues. Inside a `SKILL.md`, describe the pattern instead of pasting it.
- **Do not name people, companies or products.** The goal is better work, not shaming.
- **Test it.** Run the agent on the same few tasks with and without the anti-skill, and say in the pull request what changed. If it made no difference, it does not belong here.

## License

By contributing, you agree that your contribution is published under the MIT License of this repo.
