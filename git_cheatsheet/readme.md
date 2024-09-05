
## **Git Setup Commands**:

| Command                                         | Usage & Example                                      | Description                                                 |
|-------------------------------------------------|------------------------------------------------------|-------------------------------------------------------------|
| `git config --global user.name "Your Name"`     | `git config --global user.name "John Doe"`           | Set your global username for Git commits.                   |
| `git config --global user.email "you@example.com"` | `git config --global user.email "john@example.com"` | Set your global email for Git commits.                      |
| `git config --global --list`                    | `git config --global --list`                         | View global Git configuration settings.                     |

---

## **Basic Git Commands**:

| Command                                         | Usage & Example                                        | Description                                                 |
|-------------------------------------------------|--------------------------------------------------------|-------------------------------------------------------------|
| `git init`                                      | `git init`                                             | Initialize a new Git repository.                            |
| `git clone <repository_url>`                    | `git clone https://github.com/user/repo.git`           | Clone a remote repository to your local machine.            |
| `git status`                                    | `git status`                                           | Show the working directory status (modified, staged files).  |
| `git add <file>`                                | `git add cheatsheet.md`                                | Stage changes for a specific file to commit.                |
| `git add .`                                     | `git add .`                                            | Stage all modified files in the current directory.           |
| `git commit -m "message"`                       | `git commit -m "Initial commit"`                       | Commit staged changes with a message.                       |
| `git log`                                       | `git log`                                              | Show commit history with commit IDs and messages.            |
| `git show <commit>`                             | `git show 1a2b3c4d`                                    | Display details of a specific commit.                       |
| `git diff`                                      | `git diff`                                             | Show differences between working directory and staging area. |
| `git diff --staged`                             | `git diff --staged`                                    | Show changes between staging area and last commit.           |

---

## **Branching and Merging**:

| Command                                         | Usage & Example                                        | Description                                                 |
|-------------------------------------------------|--------------------------------------------------------|-------------------------------------------------------------|
| `git branch`                                    | `git branch`                                           | List all branches and highlight the current branch.          |
| `git branch <branch_name>`                      | `git branch feature-branch`                            | Create a new branch.                                         |
| `git checkout <branch_name>`                    | `git checkout feature-branch`                          | Switch to a different branch.                               |
| `git checkout -b <branch_name>`                 | `git checkout -b feature-branch`                       | Create and switch to a new branch at the same time.          |
| `git merge <branch_name>`                       | `git merge feature-branch`                             | Merge changes from one branch into the current branch.       |
| `git branch -d <branch_name>`                   | `git branch -d feature-branch`                         | Delete a branch after it has been merged.                   |
| `git branch -D <branch_name>`                   | `git branch -D feature-branch`                         | Forcefully delete a branch (even if not merged).             |

---

## **Stashing and Cleaning**:

| Command                                         | Usage & Example                                        | Description                                                 |
|-------------------------------------------------|--------------------------------------------------------|-------------------------------------------------------------|
| `git stash`                                     | `git stash`                                            | Stash changes without committing them, to clean the working directory. |
| `git stash apply`                               | `git stash apply`                                      | Reapply the stashed changes without removing them from the stash list. |
| `git stash pop`                                 | `git stash pop`                                        | Reapply the stashed changes and remove them from the stash list. |
| `git stash list`                                | `git stash list`                                       | View the list of stashed changes.                           |
| `git clean -fd`                                 | `git clean -fd`                                        | Remove untracked files and directories.                     |

---

## **Remote Repositories**:

| Command                                         | Usage & Example                                        | Description                                                 |
|-------------------------------------------------|--------------------------------------------------------|-------------------------------------------------------------|
| `git remote`                                    | `git remote`                                           | List all configured remotes (like `origin`).                 |
| `git remote add <name> <url>`                   | `git remote add origin https://github.com/user/repo.git`| Add a remote repository to track.                           |
| `git push <remote> <branch>`                    | `git push origin main`                                 | Push local changes to a remote branch.                      |
| `git push -u <remote> <branch>`                 | `git push -u origin main`                              | Push and set the remote branch to track the local branch.    |
| `git pull <remote> <branch>`                    | `git pull origin main`                                 | Fetch and merge changes from a remote branch.               |
| `git fetch <remote>`                            | `git fetch origin`                                     | Download changes from the remote but do not merge them.      |
| `git remote rm <name>`                          | `git remote rm origin`                                 | Remove a remote repository.                                 |

---

## **Resetting and Reverting**:

| Command                                         | Usage & Example                                        | Description                                                 |
|-------------------------------------------------|--------------------------------------------------------|-------------------------------------------------------------|
| `git reset --hard <commit>`                     | `git reset --hard HEAD~1`                              | Reset the working directory and index to a previous commit, discarding all changes. |
| `git reset --soft <commit>`                     | `git reset --soft HEAD~1`                              | Reset only the index to a previous commit, keeping changes in the working directory. |
| `git reset <file>`                              | `git reset cheatsheet.md`                              | Unstage a file without discarding changes.                  |
| `git revert <commit>`                           | `git revert 1a2b3c4d`                                  | Create a new commit that undoes the changes from a specific commit. |

---

## **Git Tagging**:

| Command                                         | Usage & Example                                        | Description                                                 |
|-------------------------------------------------|--------------------------------------------------------|-------------------------------------------------------------|
| `git tag`                                       | `git tag`                                              | List all tags in the repository.                            |
| `git tag <tag_name>`                            | `git tag v1.0`                                         | Create a new lightweight tag.                               |
| `git tag -a <tag_name> -m "message"`            | `git tag -a v1.0 -m "First release"`                   | Create an annotated tag with a message.                     |
| `git show <tag_name>`                           | `git show v1.0`                                        | Display details about a tag.                                |
| `git push <remote> <tag_name>`                  | `git push origin v1.0`                                 | Push a tag to the remote repository.                        |
| `git push --tags`                               | `git push --tags`                                      | Push all local tags to the remote repository.               |

---

## **Undoing Changes**:

| Command                                         | Usage & Example                                        | Description                                                 |
|-------------------------------------------------|--------------------------------------------------------|-------------------------------------------------------------|
| `git checkout -- <file>`                        | `git checkout -- cheatsheet.md`                        | Discard local changes to a file (revert to the last committed state). |
| `git restore <file>`                            | `git restore cheatsheet.md`                            | Another way to discard local changes (modern command).       |
| `git reset HEAD <file>`                         | `git reset HEAD cheatsheet.md`                         | Unstage a file from the staging area.                        |

---

## **Git Ignore**:
Use the `.gitignore` file to specify files and directories that Git should ignore.
Example `.gitignore`:
```
# Ignore Python compiled files
*.pyc
# Ignore directories
node_modules/
# Ignore specific files
config/local.json
```

---

## **Collaboration Workflows**:

| Command                                         | Usage & Example                                        | Description                                                 |
|-------------------------------------------------|--------------------------------------------------------|-------------------------------------------------------------|
| `git pull origin <branch>`                      | `git pull origin main`                                 | Fetch and merge changes from the remote branch.             |
| `git rebase <branch>`                           | `git rebase main`                                      | Reapply your commits on top of another branch’s history.     |
| `git cherry-pick <commit>`                      | `git cherry-pick 1a2b3c4d`                             | Apply a specific commit from another branch.                |
| `git merge --no-ff <branch>`                    | `git merge --no-ff feature-branch`                     | Force a merge commit, even if the merge could be fast-forwarded. |

---

## **Git Aliases** (Shortcuts):
You can create custom shortcuts for Git commands to speed up workflows.
Example:
```bash
git config --global alias.st status
git config --global alias.ci commit
git config --global alias.co checkout
```
Now, you can use `git st` instead of `git status`, etc.

---

## **Advanced Git Commands**:

| Command                                         | Usage & Example                                        | Description                                                 |
|-------------------------------------------------|--------------------------------------------------------|-------------------------------------------------------------|
| `git reflog`                                    | `git reflog`                                           | Show the history of all reference changes (commits, reverts). |
| `git bisect`                                    | `git bisect start`                                     | Perform a binary search through commit history to find the commit that introduced a bug. |
| `git blame <file>`                              | `git blame cheatsheet.md`                              |

 Show who made changes to each line in the file.              |
| `git archive <branch> --format=zip --output=<file>.zip` | `git archive main --format=zip --output=repo.zip` | Archive a repository to a ZIP file.                         |

---

This Git cheatsheet covers **fundamental commands** as well as **advanced workflows** for version control, branching, merging, remote management, and more. It's a helpful resource for both beginners and advanced users. Let me know if you need more details on any command!