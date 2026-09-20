# Design Deslop

An agent skill that improves interfaces through five sequential specialist passes:

**Copy → Layout → Typography → Color → Decoration**

Each specialist finds useful improvements, implements them, checks the result, and gives the manager a short done-list. The manager checks the changes and passes the current source and visual evidence to the next specialist.

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

Implementation is the default for requests to improve an editable interface. The skill preserves functionality, useful content, accessibility, and explicit brand requirements. It does not authorize deployment or new dependencies.

## What it improves

- **Copy:** repeated slogans, redundant captions, and unnecessary helper text.
- **Layout:** excessive cards, nested panels, and unsupported counter sections.
- **Typography:** weak hierarchy, small report text, and unwanted default fonts.
- **Color:** distracting gradients, unclear color roles, and contrast problems.
- **Decoration:** oversized icon tiles, excessive rounding, and unnecessary shadows.

These are design preferences, not proof that an interface was created by AI. Useful and explicitly required treatments stay in place.

## Requirements

Use an agent with source-editing tools. Subagent support enables the specialist workflow. If subagents are unavailable, the main agent performs the same passes in sequence and states this limit. Browser or screenshot tools are useful for visual checks; unavailable checks must be reported.

The package uses the standard `SKILL.md` format. Codex UI metadata is included in `agents/openai.yaml`; the main instructions do not depend on Codex-specific tool names.

## Files

- [Skill instructions](skills/design-deslop/SKILL.md)
- [Specialist references](skills/design-deslop/references)
- [Codex metadata](skills/design-deslop/agents/openai.yaml)

The package contains instructions and an icon. It does not include application code or a runtime dependency.
