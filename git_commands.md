
🚀 Basic Git Configuration
```bash
git config --global user.name "Your Name"
git config --global user.email "your.email@example.com"
git config --list                     # List all Git configs
```

📁 Repository Operations
```bash
git init                              # Initialize a new Git repository
git clone <repo_url>                  # Clone an existing repository
git remote add <name> <url>           # Add a remote repository
git remote add origin <url>           # Add a remote repository with alias 'origin'
git remote -v                         # View current dir remote repositories
git remote remove <name>              # Remove a remote
git remote set-url origin <url>       # Change remote URL
```

📂 Staging and Commit
```bash
git status                            # Check status of working directory
git add <file>                        # Stage a file
git add .                             # Stage all changes
git restore --staged <file>           # Unstage a file or directory
git commit -m "Commit message"        # Commit staged changes
git commit -am "Msg"                  # Stage and commit tracked files
git reset <file>                      # Unstage a file
git reset --hard                      # Reset working directory and index
```

🔍 Viewing Changes
```bash
git diff                              # Show unstaged changes
git diff --staged                     # Show staged changes
git diff <branch1> <branch2>          # Show differences between branches
git diff --cached                     # Show changes from last commit
git log                               # Show commit history
git log --oneline --graph             # Condensed log with branch tree
git show <commit>                     # Show details of a specific commit
```

🌿 Branching & Merging
```bash
git branch                            # List branches
git branch <branch_name>              # Create new branch
git switch <branch_name>              # Switch to branch
git checkout <branch_name>            # Switch to branch
git checkout -b <branch_name>         # Create and switch to new branch
git merge <branch_name>               # Merge into current branch
git branch -d <branch_name>           # Delete branch
git branch -D <branch_name>           # Force delete branch
git branch -m <old-name> <new-name>   # Renames the specified branch
```

⬆️⬇️ Push & Pull
```bash
git pull <url>                        # Fetches and merges changes from the remote branch.
git fetch                             # Downloads changes from the remote without merging.
git push                              # Push changes to remote from local working directory.
git push -u origin <branch_name>      # Pushes local commits to the specified branch on the remote. 
git push origin --delete <branch-name> # Deletes a branch on the remote repository.
git push --set-upstream origin <branch-name> # Pushes a new branch and sets it to track the remote branch.
```

📌 Tagging
- Tags are used to mark specific commits (e.g., for releases).
```bash
git tag                               # List tags
git tag <tagname>                     # Creates a lightweight tag
git tag -a <tagname> -m "message"     # Creates a tag with annotations an annotated tag with a message.
git push origin <tagname>             # Push tag to remote
git push origin --tags                # Push all tags to remote
git tag -d <tagname>                  # Delete local tag from local repository
git push origin --delete <tagname>    # Delete remote tag from remote repository
```

🔄 Undoing Changes
```bash
git checkout -- <file>                # Discard changes in file
git revert <commit>                   # Revert a commit by creating a new one
git reset --soft HEAD~1               # Undo last commit, keep changes staged
git reset --mixed HEAD~1              # Undo last commit, keep changes unstaged
git reset --hard HEAD~1               # Undo last commit, discard changes


🌐 Stashing
- Stashing allows you to temporarily save changes without committing.
```bash
git stash                             # Saves uncommitted changes and reverts to a clean working directory.
git stash list                        # List all stashed changes
git stash apply                       # Reapplies the most recent stash
git stash apply stash@{n}             # Reapplies a specific stash by index
git stash pop                         # Apply and delete last stashed change
git stash drop stash@{n}              # Delete a specific stashed change by index
git stash clear                       # Remove all stashed changes
```

🌿 Rebasing
- Rebasing is used to rewrite commit history or integrate changes.
```bash
git rebase <branch-name>              # Reapplies commits from the current branch onto another branch.
git rebase -i <commit-hash> # Allows editing, squashing, or reordering commits starting from specified commit.
git rebase --abort                    # Cancels an ongoing rebase and restores the previous state.
```


🧪 Advanced / Debug
```bash
git cherry-pick <commit>              # Apply commit from another branch
git rebase <branch>                   # Rebase onto another branch
git reflog                            # Show history of HEAD
git bisect start                      # Begin binary search
git blame <file>                      # Show who changed each line
git archive                           # Create archive from repository
```

Blaming
- 
```bash
git blame <file>                      # Show who changed each line
git blame 
```



🧹 Cleanup
```bash
git clean -f                          # Remove untracked files from working directory
git gc                                # Optimize repository
git prune                             # Cleanup unreachable objects
```

✅ GitHub-Specific (CLI)
# Requires GitHub CLI (gh)
```bash
gh auth login                         # Authenticate GitHub CLI
gh repo clone <user>/<repo>           # Clone GitHub repo
gh issue list                         # List issues
gh pr list                            # List PRs
gh pr create                          # Create new PR
gh pr merge                           # Merge PR
gh pr checkout <PR_number>            # Checkout PR branch


