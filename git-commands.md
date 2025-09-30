````markdown
# Git Commands Reference

This file contains Git commands I have learned, with explanations and examples. It serves as a quick reference for Git and GitHub workflow.

---

## Git Configuration

Set username and email globally:

```bash
git config --global user.name "Rahul"
git config --global user.email "rahulrahulking7777@gmail.com"
````

Check configured username and email:

```bash
git config --global user.name
git config --global user.email
```

---

## Initialize Repository

Initialize a new Git repository:

```bash
git init
```

Check repository status:

```bash
git status
git status -s  # simplified overview (Red M = modified, Green M = staged)
```

View all files including hidden ones:

```bash
ls -lart
```

---

## Staging and Committing

Add files to staging area:

```bash
git add filename      # Add specific file
git add -A            # Add all files including untracked
```

Commit changes:

```bash
git commit           # Opens editor (Vim: 'i' to insert, 'esc', then ':wq')
git commit -m "Message here"       # Direct commit with message
git commit -a -m "Message here"    # Commit all modified files directly
```

Create new file:

```bash
touch filename       # Example: touch about.html
```

Restore previous file or commit:

```bash
git checkout filename
git checkout -f                 # Force restore all files
git checkout <commit-hash>      # Restore from specific commit
```

View commit history:

```bash
git log
git log --oneline
git log -p -<number-of-logs>
```

Remove files:

```bash
git rm filename           # Delete file
git rm --cached filename  # Remove from staging only
```

View differences:

```bash
git diff             # Compare working directory with staging
git diff --staged    # Compare staging with last commit
```

---

## Ignoring Files

Create `.gitignore`:

```bash
touch .gitignore
```

Example content:

```text
mylogs.log       # Ignore all files named mylogs.log
/mylogs.log      # Ignore file only in root
*.log            # Ignore all .log files
folder_name/     # Ignore entire folder
```

---

## Branching

List branches:

```bash
git branch
```

Create and switch branches:

```bash
git branch branch_name
git checkout branch_name
git checkout -b branch_name   # Create and switch
```

Delete branches:

```bash
git branch -d branch_name    # Safe delete (merged)
git branch -D branch_name    # Force delete
```

Merge branches:

```bash
git merge branch_name   # Switch to branch to merge into first
```

---

## GitHub Integration

Add remote repository:

```bash
git remote add origin <repo-url>
git remote               # List remote names
git remote -v            # Show remote URLs
```

Push changes to GitHub:

```bash
git push origin master           # First push (may require SSH setup)
git push -u origin master        # Push and track master branch
git push -u origin branch_name   # Push other branches
```

> SSH Setup: Add your public key to GitHub to enable push/pull.

---

## Quick Notes

* Workflow: `untracked files -> add -> staging area -> commit -> repository`
* `git commit -a -m "msg"` bypasses staging for modified files
* `git status -s` shows short, color-coded status
* `git log --oneline` gives concise commit history



---
Thank you for reading! Happy Git learning! 🚀
---