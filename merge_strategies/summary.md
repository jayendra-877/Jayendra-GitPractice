# PR Merge Strategies

## Merge Commit

- Preserves the complete branch history.
- Creates an additional merge commit.
- Useful when you want to see when and how a feature branch was merged.

## Squash and Merge

- Combines all commits from a pull request into a single commit.
- Keeps the main branch history clean.
- Original branch commits do not appear individually on the target branch.

## Rebase and Merge

- Replays each commit from the feature branch onto the target branch.
- Keeps all commits separate.
- Does not create a merge commit.
- Produces a clean, linear commit history.
