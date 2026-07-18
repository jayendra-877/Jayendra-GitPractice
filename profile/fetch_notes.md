## Fetch Notes
- It fetches the information from the github
- We have git pull as well that get the changes from the github and synch local branch with github so git fetch may be going some extra work as well
- It may be just used to see the changes not change the local branch code
- extra point on fetch

## What Fetch Showed Me

- After running `git fetch origin`, my local branch was not modified.
- Git downloaded the latest commit from the remote repository.
- `git log HEAD..origin/fetch-practice --oneline` showed that the remote branch had one extra commit named "Update fetch_notes.md".
- `git diff HEAD..origin/fetch-practice` showed that the remote branch contained one additional bullet point: "extra point on fetch".
- I was able to inspect these remote changes before merging them into my local branch.
