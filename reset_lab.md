# Reset Lab
## Introduction

Learning Git reset modes.
## Soft Reset Example

Soft reset moves HEAD only.
## Hard Reset Warning

Hard reset can permanently discard uncommitted changes.

## Reset Observations

### Soft Reset
- Removes commits.
- Keeps changes staged.
- Working directory remains unchanged.

### Mixed Reset
- Removes commits.
- Unstages changes.
- Working directory keeps the changes.

### Hard Reset

- When used without specifying a commit (`git reset --hard`)
  - Resets the staging area and working directory to match the current commit (`HEAD`).
  - Discards all uncommitted changes.
  - Does **not** remove any commits.

- When used with a commit (`git reset --hard HEAD^` or `git reset --hard <commit-hash>`)
  - Moves `HEAD` to the specified commit.
  - Removes all commits that were ahead of the specified commit from the current branch history.
  - Resets the staging area and working directory to exactly match the specified commit.
  - Files become exactly as they were in that commit.