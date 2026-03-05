---
name: github_sync
description: A skill to sync the local repository with GitHub.
---

# GitHub Sync

When you are asked to sync with GitHub or use the `/sync` command, perform the following steps:

1. **Prompt the User**: Ask the user to describe the changes they have made. This description will serve as the git commit message.
2. **Execute Pull**: Run `git pull -X theirs` to pull changes from the remote, automatically resolving any conflicts in favor of the remote (theirs).
3. **Stage Changes**: Run `git add .` to stage all local modifications.
4. **Commit Changes**: Run `git commit -m "<message>"` using the description provided by the user in step 1.
5. **Push Changes**: Run `git push` to upload the local commits to GitHub.

> [!IMPORTANT]
> Ensure that the user provides a meaningful description for the commit message. If no description is provided, ask again.
