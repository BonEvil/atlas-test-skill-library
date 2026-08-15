# Install and synchronize this library

## Add the library

Ask Atlas to add or install this public HTTPS Git repository:

```text
https://github.com/BonEvil/atlas-test-skill-library.git
```

Atlas installs public HTTPS Git Skill libraries from the repository's default
branch. This repository's default branch is `main`; it contains the
`compare-options` Skill at `compare-options/SKILL.md`. Atlas discovers Skills
by recursively finding `SKILL.md` files.

## Synchronize updates

First merge the desired change into this repository's `main` branch. Then ask
Atlas to synchronize the installed library. Atlas fast-forwards the installed
library to the latest remote default-branch state.

Do not edit Atlas's installed library copy directly. Make changes in the Git
repository, follow its normal review process, and synchronize after the change
is available on `main`.

## Troubleshooting

- If Atlas cannot add the library, confirm that the URL is the public HTTPS Git
  URL above.
- If an expected update is missing, confirm it has reached `main`, then
  synchronize the installed library again.
- If a Skill is not discovered, confirm its directory contains a regular
  `SKILL.md` file. The repository's contribution guidance documents the
  required file and frontmatter format.
