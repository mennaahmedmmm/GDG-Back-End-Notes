
# Git Commands

## 1. Initialize a Repository
```bash
git init
```
- Initializes your current directory as a Git repository.

## 2. List Files with Details
```bash
ls -al
```
- Displays a detailed list of all files, including hidden ones (e.g., `.git`), in the current directory.

## 3. Change Directory
```bash
cd <folder-name>
```
- Navigates to the specified folder.

## 4. Check the Status of Your Files
```bash
git status
```
- Shows the status of files, including changes and untracked files in your repository.

## 5. List Files in the Current Directory
```bash
ls
```
- Lists all files and directories in the current folder.

## 6. Show Tracked Files in Git
```bash
git ls-files
```
- Displays all files currently tracked by Git.

## 7. View Object Details
```bash
git cat-file -p <object>
```
- Shows the content of the specified object (file or commit).

```bash
git cat-file -t <object>
```
- Displays the type of the object (blob, tree, commit).

```bash
git cat-file -s <object>
```
- Shows the size of the object.

## 8. Add Files to the Staging Area
```bash
git add <file>
```
- Adds the specified file to the staging area.

## 9. Commit Changes with a Message
```bash
git commit -m "your message"
```
- Commits changes with a descriptive message.

## 10. View Commit History
```bash
git log
```
- Displays the commit history.

## 11. Show Differences
```bash
git diff
```
- Displays the differences between your working directory and the last commit.

## 12. Show Staged Changes
```bash
git diff --staged
```
- Shows differences between staged files and the last commit.

## 13. View Details of a Specific Commit or Object
```bash
git show <SHA>
```
- Displays the details of a specific commit or object using its SHA hash.

---

## Notes

### What is a Branch?
- A branch is a separate line of development. By default, your repository starts with the `main` branch.

### What is the HEAD?
- The HEAD is a pointer to your current branch and commit, representing your position in the project's history.

---

## Undoing Changes

### 1. Remove a Repository
```bash
rm -rf .git/
```
- Deletes the Git repository from the current directory.

### 2. Unstage a Tracked File
```bash
git rm --cached <file>
```
- Untracks the specified file without deleting it.

### 3. Discard Changes in the Working Directory
```bash
git restore <file>
```
- Restores the specified file to its previous state.

### 4. Unstage a File
```bash
git restore --staged <file>
```
- Removes the file from the staging area without altering the file itself.

### 5. Change Your Last Commit Message
```bash
git commit --amend
```
- Edits the last commit message.

### 6. Revert to a Previous Commit
```bash
git reset HEAD~<number>
```
or
```bash
git reset --hard HEAD~1
```
- The `--hard` option reverts the working directory and the staging area to the specified commit.

### 7. View All Commits (Including Previous Resets)
```bash
git reflog
```
- Displays a history of all commits, including those reverted.

### 8. Revert to a Newer Commit
```bash
git reset HEAD@{<id>}
```
- Resets the working directory to a newer commit found via `git reflog`.

---

## Tagging

- Tags can mark commits as versions.
```bash
git commit -am "message"
git tag -a <version> -m "message"
```
- View a tagged version without showing all commits:
```bash
git show <version>
```

---

## Git Branching

### 1. Create a New Branch
```bash
git branch <branch-name>
```
- Creates a new branch.

### 2. Switch to Another Branch
```bash
git switch <branch-name>
```
- Switches to the specified branch.

### 3. Merge Branches
```bash
git merge <branch-name>
```
- Merges the specified branch into the current branch.

### 4. View Merged Branches
```bash
git branch --merged
```
- Lists branches that have already been merged.

### 5. Delete a Branch
```bash
git branch -d <branch-name>
```
- Deletes the specified branch.

- To rebase or resolve conflicts between branches:
```bash
git rebase main
```
---

## Working with Remotes

### 1. Clone a Repository
```bash
git clone <url> <name>
```
- Clones a remote repository. The `<name>` is optional.

### 2. View Remote Branches
```bash
git branch -r
```
- Lists all remote branches.

### 3. Fetch Changes from Remote
```bash
git fetch <remote-name>
```
- Fetches changes from the remote repository.

### 4. Pull and Merge Remote Changes
```bash
git pull <remote-name>
```
- Fetches and merges changes from the remote repository.

### 5. Push Local Changes to Remote
```bash
git push <remote-name>
```
- Pushes local changes to the remote repository.

---

## Resources

- **Visual Git Guide**: [Visual Git Guide](https://marklodato.github.io/visual-git-guide/index-en.html)
- **Git Book**: [Git Book](https://git-scm.com/book/en/v2)
- **Tutorial Video**: [AraBigData Git Repository](https://github.com/ahmedsami76/AraBigData/tree/main/Git)
- **Blog on Writing Good Commits**: [Good Commit vs Bad Commit](https://dev.to/sheraz4194/good-commit-vs-bad-commit-best-practices-for-git-1plc?ref=dailydev)

---
