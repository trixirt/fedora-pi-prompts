README.txt

fedora-rpm-patch.xml - Automated Spec File Patch Commenter

This prompt file instructs the `pi` coding agent to autonomously review and
document patches within a Fedora RPM spec file. This specific prompt
targets a common packaging bottleneck: unannotated or poorly documented patch
files in spec sources.

Usage

    pi < fedora-rpm-patch.xml

Outputs

  /tmp/<package>.spec       -> Updated spec file with documented patches
  /tmp/fedora-rpm-patch.txt -> Concise summary of all AI-generated modifications

