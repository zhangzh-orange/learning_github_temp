# GitHub Workflow Guide

```
# ===================================
# Time	 :   2024/07/26
# Author	:   Zehong Zhang
# Contact:   zhang@fmp-berlin.de
# ===================================
```

---

## 1. Clone Repository

Clone the repository to your local machine:

```
git clone <repository-url>
```

## 2. Create a New Branch

Create a new branch to save your changes, rather than committing directly to the main branch:

This command is to copy main branch's code to your own branch.

```
git checkout -b <my-feature-branch>
```

## 3. Debug or change the codes

Work on the code as needed for your feature or bug fix.

## 4. Check Differences

View the differences between your local changes and the local branch. At this point, your code is not saved into the local Git history and not committed to the remote repository (GitHub):

```
git diff
```

Press `q` to exit the diff view.

## 5. Stage Changes

Stage the changes for the next commit:

```
git add <changed-file-name>   # To add specific files
git add .                     # To add all changed files
```

## 6.Commit Changes

Commit the staged changes with a descriptive commit message:

```
git commit -m "Your commit message"
```

If you prefer to use the default editor (e.g., Vim), recommend, because in this way you can record your experiment in detail, and more easily to change with editor:

```
git commit
```

Follow these steps to write your commit message in Vim:

1. Press `i` to start editing.
2. Write your commit message.
3. Press `Esc`, then type `:wq` to save and exit edit mode.
4. Press `ZZ` (upper) to exit vim editor and back to git console.

## 7. Push Changes

Push your changes to GitHub, creating the new branch on the remote repository:

```
git push origin <my-feature>
```

You can repeat steps 3 to 7 to gradually refine the code and save it at any time. When you think your phased tasks are done, you can apply to merge your change to the main branch (steps 8 to 12).

## 8. Synchronize Branches

Sometimes, when you commit code to your branch, the main branch's code may have updates. You need to synchronize the main branch and your feature branch to ensure your updates still work. And solve the conflicts between your code and the latest main code.

### 8.1 Update Local Main Branch

Switch to the main branch:

```
git checkout main
```

Pull the latest changes from the remote main branch:

```
git pull origin main
```

### 8.2 Rebase Feature Branch

Switch back to your feature branch:

```
git checkout <my-feature-branch>
```

Rebase your feature branch onto the updated main branch:

```
git rebase main
```

Resolve any conflicts that occur during the rebase process.

### 8.3 Push Rebased Changes (Force Push)

After resolving conflicts and completing the rebase, force push your changes to the remote feature branch:

```
git push -f origin <my-feature-branch>
```

## 9. Create Pull Request

On GitHub, open a pull request to merge your feature branch into the main branch.

github => work repo => Pull requests => New pull request

## 10. Squash and Merge

The **repository maintainer** will squash and merge your pull request into the main branch on GitHub.

## 11. Delete Remote Feature Branch

After the pull request is merged, delete the remote feature branch:

On GitHub, go to the branches section and delete the merged feature branch.

## 12. Delete Local Feature Branch

Switch to the main branch and delete your local feature branch:

```
git checkout main
git branch -D <my-feature-branch>
```

## 13. Update Local Main Branch

Pull the latest updates from the remote main branch to your local repository, and start a new round of improvements:

```
git pull origin main
```

