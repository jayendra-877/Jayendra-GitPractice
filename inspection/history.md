# Git Inspection History

### 1. `git status`
**Output:**
```
On branch inspection-extra
Your branch is up to date with 'origin/inspection-extra'.

Untracked files:
  (use "git add <file>..." to include in what will be committed)
        inspection/history.md

nothing added to commit but untracked files present (use "git add" to track)
```
- **My Answer:** I am on the `inspection-extra` branch, and I have `inspection/history.md` file present untracked so the working tree is not clean

### 2. `git branch`
**Output:**
```
develop
* inspection-extra
  inspection-practice
  main
```

- **My Answer:** The local branches are `main`, `develop`, `inspection-practice`, and `inspection-extra`.

### 3. `git branch -r`
**Output:**
```
 origin/HEAD -> origin/main
  origin/develop
  origin/inspection-extra
  origin/inspection-practice
  origin/main
```

- **My Answer:** The remote branches include `main`, `develop`, `inspection-practice`, and `inspection-extra`.The origin/HEAD points to the default remote branch, which is 'main'.

### 4. `git branch -a`
**Output:**
```
  develop
* inspection-extra
  inspection-practice
  main
  remotes/origin/HEAD -> origin/main
  remotes/origin/develop
  remotes/origin/inspection-extra
  remotes/origin/inspection-practice
  remotes/origin/main
```

- **My Answer:** `git branch -a` shows both local and remote branches in one list. Difference between local and remote branch is that , local branches are listed just by their name (like `main`) and present only in the machine while the remote branches are listed with prefix `remote/origin/` (like `remotes/origin/develop`) and present in the remote server Github.

### 5. `git log --oneline`
**Output:**
```
d3a558d (HEAD -> inspection-extra, origin/inspection-extra) add extra inspection notes
0b96bd4 (origin/develop, develop) Add README with timestamp and introduction
e4d52e3 Initial commit
```

- **My Answer:** This command shows the recent commit history in a one Line format. The first commit is `Initial commit` then `Add README with timestamp and introduction` and at last `add extra inspection notes` commit.

### 6. `git log --oneline --decorate --graph --all`
**Output:**
```
* d3a558d (HEAD -> inspection-extra, origin/inspection-extra) add extra inspection notes
| * d10a641 (origin/inspection-practice, inspection-practice) add inspection practice notes
|/  
| *   e22410a (origin/main, origin/HEAD, main) Merge pull request #1 from jayendra-877/develop
| |\  
| |/  
|/|   
* | 0b96bd4 (origin/develop, develop) Add README with timestamp and introduction
|/  
* e4d52e3 Initial commit
```

- **My Answer:** After the Initial commit on the `main` branch, the `develop` branch split off and the Add README commit was made. Later, `develop` was merged into the `main` branch. After that merge, both inspection branches were created directly from the Add README commit on `develop`, so they are now running in parallel.

### 7. `git diff develop..inspection-extra`
**Output:**
```
diff --git a/inspection/extra.md b/inspection/extra.md
new file mode 100644
index 0000000..8b4bb5e
--- /dev/null
+++ b/inspection/extra.md
@@ -0,0 +1,4 @@
+## Extra Inspection Notes
+- This branch is Inspection-Extra branch
+- Learning about branches
+- Practicing Git cmds
\ No newline at end of file
```

- **My Answer:** The `inspection-extra` branch has a new file called `inspection/extra.md` with a heading and 3 bullet points compare to `develop` branch.

### 8. `git diff develop..inspection-practice`
**Output:**
```
diff --git a/inspection/notes.md b/inspection/notes.md
new file mode 100644
index 0000000..2e00714
--- /dev/null
+++ b/inspection/notes.md
@@ -0,0 +1,4 @@
+## Inspection Notes
+- Learning about Git 
+- Practicing various git commands
+- Understanding git branches
\ No newline at end of file
```

- **My Answer:** The `inspection-practice` branch has a new file called `inspection/notes.md` with a heading and 3 bullet points compare to `develop` branch, but this cmd does not compare `inspection-practice` branch with `inspection-extra` branch ,it compare `inspection-practice` with `develop` branch.

### 9. `git show d3a558d`
**Output:**
```
commit d3a558d8c640b120e451d34a8d6d86c7a896ae10 (HEAD -> inspection-extra, origin/inspection-extra)
Author: Jayendra Vishwakarma <jayendra8770@gmail.com>
Date:   Fri Jul 10 20:10:40 2026 +0530

    add extra inspection notes

diff --git a/inspection/extra.md b/inspection/extra.md
new file mode 100644
index 0000000..8b4bb5e
--- /dev/null
+++ b/inspection/extra.md
@@ -0,0 +1,4 @@
+## Extra Inspection Notes
+- This branch is Inspection-Extra branch
+- Learning about branches
+- Practicing Git cmds
\ No newline at end of file
```

- **My Answer:** This cmd shows complete information about a specific commit like author ,date and time,commit message and the new file created and what content in that file (showing this commit made a `inspection/extra.md` file and added 4 lines in it)