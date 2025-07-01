
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
git remote add origin <url>           # Add a remote repository
git remote -v                         # View remotes
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
git log                               # Show commit history
git log --oneline --graph             # Condensed log with branch tree
git show <commit>                     # Show details of a specific commit
```

🌿 Branching & Merging
```bash
git branch                            # List branches
git branch <branch_name>              # Create new branch
git checkout <branch_name>            # Switch to branch
git checkout -b <branch_name>         # Create and switch to new branch
git merge <branch_name>               # Merge into current branch
git branch -d <branch_name>           # Delete branch
git branch -D <branch_name>           # Force delete branch
```

⬆️⬇️ Push & Pull
```bash
git pull                              # Fetch and merge from remote
git fetch                             # Fetch changes from remote
git push                              # Push changes to remote
git push -u origin <branch_name>      # Push and set upstream
git push origin --delete <branch>     # Delete remote branch
```

📌 Tagging
```bash
git tag                               # List tags
git tag <tagname>                     # Create a tag
git tag -a <tagname> -m "message"     # Create annotated tag
git push origin <tagname>             # Push tag to remote
git push origin --tags                # Push all tags
git tag -d <tagname>                  # Delete local tag
git push origin --delete <tagname>    # Delete remote tag
```

🔄 Undoing Changes
```bash
git checkout -- <file>                # Discard changes in file
git revert <commit>                   # Revert a commit by creating a new one
git reset --soft HEAD~1               # Undo last commit, keep changes staged
git reset --mixed HEAD~1              # Undo last commit, keep changes unstaged
git reset --hard HEAD~1               # Undo last commit, discard changes


🌐 Stashing
```bash
git stash                             # Stash changes
git stash list                        # List stashed changes
git stash apply                       # Reapply last stash
git stash pop                         # Apply and delete last stash
git stash drop                        # Delete last stash
git stash clear                       # Remove all stashes
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

🧹 Cleanup
```bash
git clean -f                          # Remove untracked files
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
