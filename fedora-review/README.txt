fedora-rpm-*.xml - Automated Fedora RPM Spec File Assistant Prompts

These prompt files instruct the `pi` coding agent to autonomously review and
modify Fedora RPM spec files to ensure compliance with Fedora packaging
guidelines.

Usage

    pi < fedora-rpm-<prompt>.xml

Prompts
------------------------------------------------------------------------

fedora-rpm-english.xml
  Ensures the specfile uses American English spelling and corrects
  common typos. Complies with the requirement: "Spec file is legible
  and written in American English."

fedora-rpm-extra-bins.xml
  Scans source tarballs for unintended binary files (ELF, PE, WASM)
  and adds %prep rules to remove them. Complies with: "Sources
  contain only permissible code or content."

fedora-rpm-fonts.xml
  Scans the built RPM for embedded font files and adds %prep rules
  to remove them, as embedded fonts are generally prohibited in RPMs.

fedora-rpm-globals.xml
  Replaces hardcoded version/release literals with %global variables
  for better maintainability, and removes unused globals.

fedora-rpm-macros.xml
  Replaces hardcoded directory paths (e.g., /usr/bin) with standard
  RPM macros (e.g., %{_bindir}) to ensure architecture independence.

fedora-rpm-patch.xml
  Reviews and documents unannotated or poorly documented patch files
  within the spec file sources.

fedora-rpm-preserve-time.xml
  Checks copy/install commands in %prep, %build, and %install stages
  and adds timestamp preservation flags where appropriate. Complies
  with: "Packages should try to preserve timestamps of original
  installed files."

Outputs (for all prompts)
  /tmp/<package>.spec       -> Updated spec file with suggested changes
  /tmp/fedora-rpm-*.txt     -> Concise summary of AI-generated modifications
