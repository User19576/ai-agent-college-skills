# Filesystem and Share Evidence

Use when reviewing permissions, ownership, or network-share claims in technical coursework. Keep feedback factual and brief; do not supply assessed explanatory paragraphs. These are interpretation rules, not evidence that a learner's filesystem or share has been tested.

## Review sequence

1. Identify the object and command. Read the exact path, VM identity, and invocation; distinguish `ls -ld DIRECTORY`, which lists the directory itself, from commands listing its contents. Separate learner-reported execution, the command's scope, and screenshot-confirmed results; a command listed in prose does not prove its result for every object.
2. Interpret the mode correctly. The leading `d` in `drwxrwxrwx` identifies a directory; an ordinary file with mode 777 displays `-rwxrwxrwx`. Do not describe the leading character as a permission bit or apply a directory mode string to regular files.
3. Separate directory and file semantics. Directory `r` permits listing names, `w` permits modifying directory entries subject to other checks, and `x` permits search/traversal. File `x` concerns execution; directory `x` alone does not make a contained file executable. These mode bits are not a guarantee that every operation succeeds, because other access controls or mount options may apply.
4. Check recursive scope. Recursive `chmod` and `chown` concern existing objects reached during execution; they do not establish inherited permissions or ownership for files created later. Credit the learner-reported recursive command without claiming that a directory-only screenshot verifies each contained file's mode or owner. Report execution errors or unshown outcomes as limits, not successful changes.
5. Bound share claims. Matching owner/group/mode on a local export directory and a client mount point does not alone prove an NFS mount. Matching file contents on two VMs show the observed contents, not independently the export configuration, mount source, or remote edit. Request mount-source output such as `findmnt -T PATH` only for a genuine requirement or unresolved mount claim, not to expand an already agreed review scope.
6. Report the smallest correction. Distinguish what a command is intended to set from what the screenshot confirms. Do not demand recursive file listings when the learner intentionally supplied directory evidence and makes no claim that individual file modes were verified. Apply these distinctions to the actual evidence before claiming a coursework finding.

## Verification

Each finding identifies the command or observed output and its scope. Unshown child-object results, inheritance, mount source, export configuration, and remote edits remain unverified unless separately evidenced. Do not execute lab commands merely to review a report or describe source review as a filesystem/share test.
