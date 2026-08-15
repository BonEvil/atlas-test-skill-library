# Contributing

Contributions must preserve the existing Skills unless the change explicitly
targets them. For the current Skill, that means leaving
`compare-options/SKILL.md` and `compare-options/agents/openai.yaml` unchanged
when changing repository documentation.

## Skill layout

Each Skill is a directory containing a `SKILL.md`. The existing layout is:

```text
compare-options/
├── SKILL.md                 # required Skill definition
└── agents/
    └── openai.yaml          # optional repository metadata
```

Atlas recursively discovers `SKILL.md` files. It does not currently consume
`compare-options/agents/openai.yaml`; extra files are optional, not required.
Do not use a symbolic link for `SKILL.md`.

## Required `SKILL.md` frontmatter

`SKILL.md` must be UTF-8 text with YAML frontmatter beginning on the first line.
The frontmatter has exactly two keys: `name` and `description`. `name` is
lowercase kebab-case; `description` is a non-empty string no longer than 1,024
characters and must begin with `Use when` followed by a trigger. The instruction
body after the frontmatter must be non-empty.

The current `compare-options/SKILL.md` uses this shape:

```yaml
---
name: compare-options
description: Use when the user needs to compare two or more choices and decide between them.
---
```

Write `Use when` as a concrete activation sentence, not a label. For example,
the description above identifies the user situation that should activate
`compare-options`.

## Validation checklist

Before submitting a change:

- Confirm every Skill directory has a non-symlink `SKILL.md` and that its body is non-empty.
- Check that frontmatter has only `name` and `description`, with a kebab-case name and a concrete `Use when` trigger.
- Check claims against current Atlas library behavior; do not claim that optional files are scanned or consumed.
- Render or structurally inspect Markdown: headings, lists, fenced code blocks, and relative links must be readable and valid.
- Resolve each relative link with exact filename casing and compare documented paths with the tracked tree.
- Preserve unrelated Skills byte-for-byte; for documentation-only work, verify `compare-options/SKILL.md` and `compare-options/agents/openai.yaml` are unchanged.
- Run `git diff --check` and review the complete diff for unintended files or whitespace errors.
