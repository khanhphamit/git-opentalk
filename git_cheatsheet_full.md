
# GIT COMMANDS CHEATSHEET (FULL GUIDE)
**From Beginner to Advanced**

---

## 🧱 GETTING STARTED

```bash
git --version
# Check installed Git version

git config --global user.name "Your Name"
git config --global user.email "you@example.com"
# Set global Git username and email

git init
# Initialize a new Git repository in current folder

git help
# Show general Git help

git help <command>
# Show help for specific Git command
```

---

## 🌐 WORKING WITH REMOTE REPOSITORIES

```bash
git clone <repo-url>
# Clone a repository to your local machine

git remote -v
# Show current remote repositories

git remote add origin <url>
# Add a remote repository (usually called "origin")

git remote remove origin
# Remove a remote repository
```

---

## ✏️ STAGING AND COMMITTING

```bash
git status
# Show current state: staged, modified, untracked files

git add <filename>
# Stage a single file

git add .
# Stage all changes (new/modified/deleted files)

git reset <file>
# Unstage a file (remove from staging)

git commit -m "Message"
# Commit staged changes with message

git commit -am "Message"
# Stage and commit all tracked changes (skip 'add')
```

---

## 🔄 PUSHING & PULLING

```bash
git push -u origin main
# Push your local commits to the remote repository (and set upstream)

git push
# Push latest changes to remote

git pull origin main
# Pull changes from remote main branch and merge

git fetch
# Download changes from remote without merging

git fetch --all
# Fetch all branches from all remotes

git pull --rebase
# Pull using rebase instead of merge
```

---

## 🌿 BRANCHING

```bash
git branch
# List local branches

git branch <branch-name>
# Create a new branch

git checkout <branch-name>
# Switch to another branch

git checkout -b <branch-name>
# Create and switch to a new branch

git switch <branch-name>
# Modern syntax to switch branches (Git 2.23+)

git switch -c <branch-name>
# Create and switch to a new branch

git branch -d <branch-name>
# Delete local branch (only if merged)

git branch -D <branch-name>
# Force delete local branch
```

---

## 🔀 MERGING

```bash
git merge <branch-name>
# Merge specified branch into current branch

git merge --no-ff <branch-name>
# Merge with a commit even if fast-forward is possible
```

> **Conflict resolution:**
> Git will show conflict markers:
> ```diff
> <<<<<<< HEAD
> current change
> =======
> incoming change
> >>>>>>> branch-name
> ```
> You must manually edit and resolve before committing.

---

## 🧹 REBASE & SQUASH

```bash
git rebase <base-branch>
# Reapply commits on top of base-branch

git rebase -i HEAD~3
# Interactively rebase last 3 commits (squash, edit, etc.)

# In the interactive screen:
# pick    → keep the commit
# squash  → combine with previous commit

git rebase --abort
# Abort current rebase

git rebase --continue
# Continue rebase after conflict resolution
```

---

## 📜 LOGS & HISTORY

```bash
git log
# Show commit history

git log --oneline --graph --all
# Compact graph view of commits

git show <commit-hash>
# Show details of a specific commit

git diff
# Show unstaged changes

git diff --staged
# Show staged changes

git blame <file>
# Show who edited each line last
```

---

## 🔄 RESET & UNDO

```bash
git checkout <commit> <file>
# Restore a file from an earlier commit

git restore <file>
# Discard changes in working directory (Git 2.23+)

git reset <file>
# Unstage a file

git reset --hard HEAD
# Discard all changes (dangerous!)

git reset --hard <commit>
# Reset to a specific commit (dangerous!)

git revert <commit>
# Create a new commit that undoes a previous commit (safe)


git reset --soft <commit>
```

---

## 🏷️ TAGGING

```bash
git tag
# List tags

git tag v1.0
# Create lightweight tag

git tag -a v1.0 -m "Release v1.0"
# Create annotated tag

git push origin v1.0
# Push a tag to remote
```

---

## 🙈 .GITIGNORE

Create a `.gitignore` file to exclude files/folders from tracking:

```
node_modules/
.env
*.log
dist/
*.tmp
*.DS_Store
```

---

## 📥 STASHING CHANGES

```bash
git stash
# Save uncommitted changes temporarily

git stash list
# List all stashes

git stash apply
# Apply latest stash

git stash apply stash@{1}
# Apply a specific stash

git stash drop
# Delete latest stash

git stash clear
# Clear all stashes
```

---

## ✂️ ALIASES (CONFIG SHORTCUTS)

```bash
git config --global alias.co checkout
git config --global alias.br branch
git config --global alias.ci commit
git config --global alias.st status
git config --global alias.last "log -1 HEAD"
git config --global alias.unstage "reset HEAD --"
```

**Example:**
```bash
git co main
# (means: git checkout main)
```

---

## 🧼 GIT CLEAN (REMOVE UNTRACKED FILES)

```bash
git clean -n
# Preview what will be deleted

git clean -f
# Force delete untracked files

git clean -fd
# Delete untracked files and directories
```

---

## 🔗 ADVANCED: SUBMODULES

```bash
git submodule add <repo-url> <path>
# Add a Git repository as a submodule

git submodule init
git submodule update
# Initialize and update submodules
```

---

## 🧯 TROUBLESHOOTING

```bash
git fsck
# Check internal Git consistency

git gc
# Garbage collection, optimize storage

git reflog
# Show history of HEAD (even for deleted commits)

git cherry-pick <commit>
# Apply a single commit from another branch
```

---

## 🧠 SUMMARY

- Git is powerful for version control:
  - Use branches for safe feature development
  - Use commits and messages clearly
  - Rebase for cleaner history (but merge for teams)
  - Use `.gitignore` to avoid clutter
  - Push/Pull to sync with team
  - Use stash/reset/revert to manage mistakes

---

**Happy Git-ing!**
