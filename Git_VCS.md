
# **source code management**

Below is a comprehensive list of commonly used Git commands for **source code management** and **branch management**, organized by category for clarity. These commands assume you're working in a Git repository.

---

### **1. Initializing and Configuring a Repository**
- **Initialize a new Git repository**:
  ```bash
  git init
  ```
  - Creates a new Git repository in the current directory.

- **Clone a repository**:
  ```bash
  git clone <repository-url>
  ```
  - Downloads a repository from a remote source (e.g., GitHub, GitLab).

- **Set user information** (for commits):
  ```bash
  git config --global user.name "Your Name"
  git config --global user.email "your.email@example.com"
  ```

- **Check repository configuration**:
  ```bash
  git config --list
  ```

---

### **2. Source Code Management**
These commands help manage changes to your codebase.

- **Check status of working directory**:
  ```bash
  git status
  ```
  - Shows the current state of the working directory and staging area.

- **Add files to staging**:
  ```bash
  git add <file>
  git add .
  ```
  - Stages specific files or all changes for the next commit.

- **Commit changes**:
  ```bash
  git commit -m "Commit message"
  ```
  - Saves staged changes to the repository with a descriptive message.

- **Amend the last commit**:
  ```bash
  git commit --amend
  ```
  - Modifies the most recent commit (e.g., to edit the message or add files).

- **View commit history**:
  ```bash
  git log
  git log --oneline
  ```
  - Displays the commit history (use `--oneline` for a concise view).

- **View changes**:
  ```bash
  git diff
  ```
  - Shows differences between the working directory and the last commit.

- **Restore or discard changes**:
  ```bash
  git restore <file>
  git restore --staged <file>
  ```
  - Discards changes in the working directory or unstages a file.

- **Remove files**:
  ```bash
  git rm <file>
  ```
  - Removes a file from the working directory and stages the deletion.

- **Move or rename files**:
  ```bash
  git mv <old-name> <new-name>
  ```
  - Renames or moves a file and stages the change.

---

### **3. Branch Management**
- These commands are used to create, manage, and work with branches.

- **List all branches**:
  ```bash
  git branch
  git branch -a
  ```
  - Shows local branches (`-a` includes remote branches).

- **Create a new branch**:
  ```bash
  git branch <branch-name>
  ```
  - Creates a new branch but doesn’t switch to it.

- **Switch to a branch**:
  ```bash
  git checkout <branch-name>
  ```
  - Switches to the specified branch.

- **Create and switch to a new branch**:
  ```bash
  git checkout -b <branch-name>
  ```
  - Creates a new branch and switches to it in one command.

- **Merge a branch**:
  ```bash
  git merge <branch-name>
  ```
  - Merges the specified branch into the current branch.

- **Delete a branch**:
  ```bash
  git branch -d <branch-name>
  git branch -D <branch-name>
  ```
  - Deletes a branch (`-d` for merged branches, `-D` to force delete unmerged branches).

- **Rename a branch**:
  ```bash
  git branch -m <old-name> <new-name>
  ```
  - Renames the specified branch.

- **View branch differences**:
  ```bash
  git diff <branch1> <branch2>
  ```
  - Shows differences between two branches.

---

### **4. Remote Repository Management**
- These commands manage interactions with remote repositories.

- **Add a remote repository**:
  ```bash
  git remote add <name> <url>
  ```
  - Links a remote repository (e.g., `git remote add origin <url>`).

- **View remote repositories**:
  ```bash
  git remote -v
  ```
  - Lists all remote repositories and their URLs.

- **Push changes to a remote**:
  ```bash
  git push origin <branch-name>
  ```
  - Pushes local commits to the specified branch on the remote.

- **Fetch changes from a remote**:
  ```bash
  git fetch origin
  ```
  - Downloads changes from the remote without merging.

- **Pull changes from a remote**:
  ```bash
  git pull origin <branch-name>
  ```
  - Fetches and merges changes from the remote branch.

- **Push a new branch to remote**:
  ```bash
  git push --set-upstream origin <branch-name>
  ```
  - Pushes a new branch and sets it to track the remote branch.

- **Delete a remote branch**:
  ```bash
  git push origin --delete <branch-name>
  ```
  - Deletes a branch on the remote repository.

---

### **5. Stashing Changes**
- Stashing allows you to temporarily save changes without committing.

- **Stash changes**:
  ```bash
  git stash
  ```
  - Saves uncommitted changes and reverts to a clean working directory.

- **List stashes**:
  ```bash
  git stash list
  ```
  - Shows all stashed changes.

- **Apply a stash**:
  ```bash
  git stash apply
  git stash apply stash@{n}
  ```
  - Reapplies the most recent stash or a specific stash (`n` is the stash index).

- **Drop a stash**:
  ```bash
  git stash drop stash@{n}
  ```
  - Removes a specific stash.

- **Clear all stashes**:
  ```bash
  git stash clear
  ```
  - Deletes all stashed changes.

---

### **6. Rebasing**
- Rebasing is used to rewrite commit history or integrate changes.

- **Rebase a branch**:
  ```bash
  git rebase <branch-name>
  ```
  - Reapplies commits from the current branch onto another branch.

- **Interactive rebase**:
  ```bash
  git rebase -i <commit-hash>
  ```
  - Allows editing, squashing, or reordering commits starting from the specified commit.

- **Abort a rebase**:
  ```bash
  git rebase --abort
  ```
  - Cancels an ongoing rebase and restores the previous state.

---

### **7. Undoing Changes**
- These commands help revert or undo changes.

- **Reset to a previous commit**:
  ```bash
  git reset <commit-hash>
  git reset --hard <commit-hash>
  ```
  - Resets the branch to a specific commit (`--hard` discards changes).

- **Revert a commit**:
  ```bash
  git revert <commit-hash>
  ```
  - Creates a new commit that undoes the changes from the specified commit.

---

### **8. Tagging**
- Tags are used to mark specific commits (e.g., for releases).

- **Create a tag**:
  ```bash
  git tag <tag-name>
  git tag -a <tag-name> -m "Tag message"
  ```
  - Creates a lightweight tag or anopening annotations an annotated tag with a message.

- **List tags**:
  ```bash
  git tag
  ```
  - Shows all tags in the repository.

- **Push tags to remote**:
  ```bash
  git push origin <tag-name>
  ```
  - Pushes a tag to the remote repository.

- **Delete a tag**:
  ```bash
  git tag -d <tag-name>
  ```
  - Deletes a local tag.

---

### **9. Viewing and Managing History**
- **Show detailed commit info**:
  ```bash
  git show <commit-hash>
  ```
  - Displays details of a specific commit.

- **Blame a file**:
  ```bash
  git blame <file>
  ```
  - Shows who last modified each line of a file.

- **Clean untracked files**:
  ```bash
  git clean -f
  ```
  - Removes untracked files from the working directory.


---


### **10. Common Workflows**
- Here are some common Git workflows for source code and branch management:

- **Create a feature branch and push it**:
  ```bash
  git checkout -b feature-branch
  git add .
  git commit -m "Add new feature"
  git push --set-upstream origin feature-branch
  ```

- **Merge feature branch into main**:
  ```bash
  git checkout main
  git pull origin main
  git merge feature-branch
  git push origin main
  ```

- **Resolve merge conflicts**:
  1. Run `git merge <branch-name>` and encounter conflicts.
  2. Edit the conflicting files to resolve conflicts (marked by `<<<<<<<`, `=======`, `>>>>>>>`).
  3. Stage resolved files: `git add <file>`.
  4. Complete the merge: `git commit`.

- **Rebase a feature branch onto main**:
  ```bash
  git checkout feature-branch
  git rebase main
  git push --force
  ```
  - (Use with caution due to history rewrite.)

---

### **Tips**
- **Always pull before pushing**: To avoid conflicts, run `git pull` to ensure your local branch is up-to-date.
- **Use meaningful commit messages**: Describe the purpose of the changes clearly.
- **Backup before destructive commands**: Commands like `git reset --hard` or `git push --force` can cause data loss.
- **Use `.gitignore`**: Create a `.gitignore` file to exclude files (e.g., `node_modules/`, `.env`) from version control.

---
