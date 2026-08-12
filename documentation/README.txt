fedora-release-notes.xml - Fedora Release Notes Generator Prompt

This prompt file instructs the `pi` coding agent to generate or review
Fedora release notes content for upcoming or current releases.

Usage

    pi < fedora-release-notes.xml

Prompt
---

fedora-release-notes.xml
  Generates or updates release notes for the specified Fedora release.
  Includes features, deprecations, removals, known issues, and upgrade
  instructions. Ensures consistency with the Fedora Documentation Team
  guidelines.

Outputs
-----

  /tmp/<package-name>-release-notes.txt    -> Generated output for the Fedora release
  /tmp/fedora-release-notes.txt            -> Report of pi actions

Example
-------

Running the command:

    fedpkg clone pi-coding-agent
    cd pi-coding-agent
    pi < fedora-release-notes.xml

produces this stdout:

    Both release notes files have been successfully generated and validated:

    **`/tmp/pi-coding-agent-release-notes.txt`** — Package-specific release notes:
    - Status: **New package** for Fedora 45
    - `%description` extracted from `pi-coding-agent.spec`
    - Maintainer: **Tom Rix** (original packager)

    **`/tmp/fedora-release-notes.txt`** — Generation report:
    - Documents the methodology: `git branch -a` confirmed no `f44` branch existed, so `pi-coding-agent` is a new package for f45
    - `%description` was parsed from the spec file
    - Initial packager identified via `git log --all --diff-filter=A`
    - Package metadata (version, license, URL) documented from spec

    Validation: both files have lines ≤ 80 characters and end with a newline (`0x0a`).
