# Contributing

Contributions are welcome -- particularly from practising CS leaders and operators who see gaps, disagree with a framework, or have a skill that should exist but does not.

## What Makes a Good Contribution

- New standalone skills that fill gaps in the library (a skill that would help a CSM manage accounts better)
- Improvements to existing skills based on real-world use (you tried a skill, found a gap, and improved it)
- Corrections to frameworks, scoring models, or best practices based on operating experience
- Bug fixes in YAML frontmatter, broken links, or formatting issues

## Skill Standards

Every skill in this repo follows the [Agent Skills](https://agentskills.io) open standard. Before submitting a new skill or modifying an existing one:

1. **YAML frontmatter** must include `name`, `description`, `license: MIT`, and `metadata` with `author`, `version`, and `standalone: true`
2. **Name** must be lowercase with hyphens, match the directory name, and be 1-64 characters
3. **Description** must be under 1024 characters and include both "Use when" primary triggers and "Also triggers" secondary triggers
4. **Zero dependencies** on other skills. Every standalone skill works in isolation
5. **Zero em-dashes.** Use double hyphens (--) throughout
6. **No invented case studies or fictional client examples.** Use frameworks, logic, and industry observations
7. **Opinionated.** Skills take positions on what good CS looks like. Generic advice is not a skill

## Quality Bar

- Every skill should produce an output a senior CSM would find useful, not just formatted
- Frameworks should encode judgment, not just structure. A scoring model with thresholds and interpretation is more valuable than a blank template
- Quality gates and principles sections are required. The skill should tell the user how to evaluate whether the output is good enough
- Target depth: 100-170 lines, 1000-1500 words. Deep enough to be useful, concise enough to fit in a context window

## Process

1. Fork the repo
2. Create a new branch for your contribution
3. Add or modify the skill in the `skills/` directory
4. Ensure the SKILL.md passes the [agentskills.io validator](https://github.com/agentskills/agentskills/tree/main/skills-ref)
5. Submit a pull request with a clear description of what the skill does and why it belongs in the library

## What This Repo Is Not

- Not a collection of prompt templates. Skills encode frameworks and judgment, not just formatting
- Not a substitute for CS expertise. The skills amplify what a CSM already knows -- they do not replace the need to know the domain
- Not a product. This is open-source IP shared under MIT licence. Use it, fork it, adapt it

## Questions

Open an issue in this repo.
