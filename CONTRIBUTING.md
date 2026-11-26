# Contributing

Anti-skills only work if they come from real bad output that a person actually saw. Contributions are welcome. Please read this first.

## Add a rule to an existing anti-skill

1. Open an issue or a pull request against the skill's `SKILL.md`.
2. Write the rule as one line that says what not to do, then one short sentence on why it fails.
3. Say where the pattern came from, in general terms. For example, "three cold emails to an open source maintainer in 2026". Do not name the sender.

## Add a new anti-skill

1. Create a folder `skills/<name>/` with a `SKILL.md` inside. Use lowercase letters and hyphens for the name.
2. Start the file with the two required fields:

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

## Rules for every contribution

- **Base it on things you received or reviewed yourself.** You may use AI to help with the wording, but you must have seen each pattern with your own eyes. That is the point of this repo.
- **Do not paste the original messages, code or text.** They contain other people's personal data and words. Describe the pattern instead.
- **Do not name people, companies or products.** The goal is better work, not shaming.
- **Test it.** Run the agent on the same few tasks with and without the anti-skill, and say in the pull request what changed. If it made no difference, it does not belong here.
