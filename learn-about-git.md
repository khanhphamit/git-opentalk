# Mastering Git: From Zero to Hero
## Learn Git from Basic to Pro  
*Presented by: khanh.phamvan*  
*Date: 2025-07-18*

---

# Presentation Overview

- What is Git?  
- Why use Git?  
- Git Core Concepts  
- Basic Workflow  
- Branching & Merging  
- Merge Conflicts  
- Undoing Mistakes  
- .gitignore  
- Tagging  
- Rebase & Squash  
- Git Workflows  
- Best Practices  
- Tools & Aliases  
- Recap  
- Q&A  

---

# What is Git?

- A **Distributed Version Control System**  
- Created by **Linus Torvalds** in 2005  
- Tracks code history, supports collaboration  
- Works locally and remotely

---

# Why Use Git?

- Code backup & version tracking  
- Enables team collaboration  
- Multiple developers, one repo  
- Supports branching, merging, rollback

---

# Core Git Concepts

| Term       | Description                      |
|------------|----------------------------------|
| Repo       | The project directory             |
| Commit     | Snapshot of current changes       |
| Branch     | Independent line of development   |
| Merge      | Integrate changes between branches|
| Clone      | Copy remote repo to local         |
| Push/Pull  | Sync with remote server           |

---

# Basic Git Workflow

```bash
git init                      # Start Git in current folder
git status                    # Check status
git add <file>                # Stage files
git commit -m "Message"       # Save commit
git remote add origin <url>   # Link to remote repo
git push -u origin main       # Push to remote
--commit B1