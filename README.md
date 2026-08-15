# Atlas test Skill library

This repository is a small Atlas repository-backed Skill library. It currently
ships the `compare-options` Skill, which helps users make an explicit,
criteria-based choice between options.

## Repository layout

```text
.
├── README.md
├── CONTRIBUTING.md
└── compare-options/
    ├── SKILL.md
    └── agents/
        └── openai.yaml
```

Atlas discovers Skills by recursively finding `SKILL.md` files. In this
repository, the Skill definition is
[`compare-options/SKILL.md`](compare-options/SKILL.md). The accompanying
`compare-options/agents/openai.yaml` is optional repository content; Atlas's
current Skill scanner reads `SKILL.md`, not that file.

## Add this library to Atlas

Ask Atlas to add or install this repository using its public HTTPS Git URL:

```text
https://github.com/BonEvil/atlas-test-skill-library.git
```

Atlas clones the repository's default branch and scans it for Skills. An
install requires at least one `SKILL.md`; invalid Skill entries are recorded
individually while valid ones remain usable.

## Synchronization and maintenance

This repository's default branch is `main`. Synchronizing the installed library
fast-forwards it to the latest remote `main` state. Atlas preserves each
Skill's enabled state and resolved invocation alias across synchronization,
using its relative path.

Do not edit an installed Atlas library copy directly. Make documentation or
Skill changes in this Git repository, contribute them through the repository's
normal review process, and then synchronize the installed library. See
[CONTRIBUTING.md](CONTRIBUTING.md) for the Skill contract and review checklist.
