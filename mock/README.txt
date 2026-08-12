fedora-rpm-changelog.xml - Fedora RPM Spec File Changelog Assistant

This prompt instructs the `pi` coding agent to review `git diff` output and
update the spec file's `%changelog` section with relevant entries.

Usage

    pi < fedora-rpm-changelog.xml

Prompts
---
fedora-rpm-changelog.xml
  Summarizes current `git diff` changes into the spec file's `%changelog`.
  It uses `git config` for author info and `date` for today's date.
  It handles `%autochangelog` and avoids overwriting existing entries.

Recommendation
---
It is recommended to use the GUI diff tool `diffuse` to review and merge the
suggested changes. `diffuse` allows line-by-line merging, enabling the
developer to filter out unneeded change lines.

Example:
    diffuse hiplaslt.spec /tmp/hiplaslt.spec

Outputs
---
  /tmp/<package>.spec       -> Updated spec file with generated changelog
  /tmp/fedora-rpm-changelog.txt -> Summary of the generated changelog entry