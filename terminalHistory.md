# Terminal History

## Cherry Pick

```
git cherry-pick 1eb7b66
```

```
[capstone-feature 5f11010] add git lessons
 Date: Tue Jul 21 14:10:07 2026 +0530
 2 files changed, 7 insertions(+)
 create mode 100644 journal/git_lessons.md
 create mode 100644 terminalHistory.md
```

---

## Rebase

```
git fetch origin
git rebase origin/develop
```
```
remote: Enumerating objects: 1, done.
remote: Counting objects: 100% (1/1), done.
remote: Total 1 (delta 0), reused 0 (delta 0), pack-reused 0 (from 0)
Unpacking objects: 100% (1/1), 889 bytes | 80.00 KiB/s, done.
From github.com:jayendra-877/Jayendra-GitPractice
   2d3b8d7..4daf7a9  develop    -> origin/develop

Auto-merging README.md
CONFLICT (content): Merge conflict in README.md
error: could not apply 4a61ec3... add conflict progress
hint: Resolve all conflicts manually, mark them as resolved with
hint: "git add/rm <conflicted_files>", then run "git rebase --continue".
hint: You can instead skip this commit: run "git rebase --skip".
hint: To abort and get back to the state before "git rebase", run "git rebase --abort".
hint: Disable this message with "git config set advice.mergeConflict false"
Could not apply 4a61ec3... # add conflict progress
```

---

## Force With Lease

```
git push --force-with-lease
```

```
Enumerating objects: 5, done.
Counting objects: 100% (5/5), done.
Delta compression using up to 18 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 377 bytes | 377.00 KiB/s, done.
Total 3 (delta 2), reused 0 (delta 0), pack-reused 0 (from 0)
remote: Resolving deltas: 100% (2/2), completed with 2 local objects.
To github.com:jayendra-877/Jayendra-GitPractice.git
 + 4a61ec3...beb45ef capstone-conflict -> capstone-conflict (forced update)
```

---

## Revert

```
git revert --no-edit 2bc19dd
```

```
[capstone-conflict 89fbbf3] Revert "add incorrect program entry"
 Date: Tue Jul 21 14:22:20 2026 +0530
 1 file changed, 2 deletions(-)
```
