## Force With Lease Lab

### First Commit

Learning about rebasing.

### Second Commit

Learning about rebasing 2.


## What Changed After Rebase

Before rebasing, the commits had one set of commit hashes.

After rebasing onto origin/develop, Git created new commits with new hashes because the parent commit changed.

Although the commit messages stayed the same, the commit IDs changed.

A normal push was rejected because the remote branch had different history.

Using:

git push --force-with-lease

updated the remote safely.

## Why --force-with-lease Is Safer

- It checks whether the remote branch has changed.
- It prevents overwriting someone else's work.
- It is safer than --force because it only rewrites history if the remote branch is exactly what Git expects.