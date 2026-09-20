# Design Deslop

An agent skill that improves interfaces through five review areas, one at a time:

**Copy → Layout → Typography → Color → Decoration**

For a small interface, one reviewer checks all five areas in sequence. Separate specialist agents are optional. Each reviewer finds useful improvements, makes changes, and records which pages, screen sizes, and states were checked. When specialists are used, the manager supplies current source paths and screenshots. Each specialist must confirm that it opened the images before making visual judgments.

## Install

Install through the [skills CLI](https://skills.sh/docs/cli):

```sh
npx skills add dennisko/design-deslop --skill design-deslop
```

Install globally for Codex:

```sh
npx skills add dennisko/design-deslop --skill design-deslop --agent codex --global
```

List the available skill without installing:

```sh
npx skills add dennisko/design-deslop --list
```

## Use

Ask your agent:

> Use design-deslop on the landing page. Save full-page before and after screenshots.

For a review without changes:

> Use design-deslop to review the dashboard. Do not edit files.

The skill makes changes when you ask it to improve an editable interface. It keeps product functions, useful content, accessibility features, and required brand elements. It does not permit deployment or new dependencies.

## What it improves

- **Copy:** repeated slogans, repeated captions, and unnecessary help text.
- **Layout:** too many cards, panels inside panels, and unnecessary groups of numbers.
- **Typography:** unclear text order, small report text, and unwanted default fonts.
- **Color:** gradients that compete with content, unclear color purposes, and contrast problems.
- **Decoration:** large icon tiles, excessive corner rounding, and unnecessary shadows.

These patterns describe design preferences. They do not prove that AI made the interface. Useful and required design elements remain.

## Requirements

Use an agent with tools that can edit source files. Subagents are optional. Browser or screenshot tools help with visual checks. The agent must report checks that it cannot complete, including affected screen states it did not inspect.

The package uses the standard `SKILL.md` format. The `agents/openai.yaml` file contains Codex interface settings. The main instructions do not require specific Codex tool names.

## Files

- [Skill instructions](skills/design-deslop/SKILL.md)
- [Review references](skills/design-deslop/references)
- [Codex metadata](skills/design-deslop/agents/openai.yaml)

The package contains instructions and an icon. It contains no application code and requires no additional runtime package.
