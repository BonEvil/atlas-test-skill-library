# Skill authoring checklist

- [ ] Put the Skill in a directory containing a non-symlink `SKILL.md` file.
- [ ] Start `SKILL.md` with YAML frontmatter on its first line. Include exactly
  the `name` and `description` keys.
- [ ] Set `name` to lowercase kebab-case.
- [ ] Make `description` a non-empty string of at most 1,024 characters that
  begins with a concrete `Use when ...` activation sentence.
- [ ] Write a non-empty instruction body after the frontmatter.
- [ ] Keep the Markdown structurally readable: headings, lists, fenced code
  blocks, and relative links must be valid; resolve relative links using their
  exact tracked filename casing.
- [ ] Preserve unrelated Skills byte-for-byte.
