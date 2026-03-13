# Git Fundamentals 

##  What is Git?

Git is a **version control system**.

It helps developers:

- Track changes in code
    
- Work with teams
    
- Restore previous versions
    
- Develop features without breaking main code
    

Example problem without Git:

```
calculator_v1.sh
calculator_v2.sh
calculator_final.sh
calculator_final_final.sh
calculator_last.sh
```

Git solves this by **tracking history automatically**.

---

##  Git Workflow (Important Concept)

Explain this **3-stage model**.

```
Working Directory → Staging Area → Repository
```

|Stage|Meaning|
|---|---|
|Working Directory|Where you edit files|
|Staging Area|Preparing files for commit|
|Repository|Permanent history|

Example flow:

```
edit file → git add → git commit
```

---

# Core Git Commands

---

##  `git init`

Purpose: **Create a new Git repository**

Command:

```bash
git init
```

What happens:

- Creates `.git` folder
    
- Git starts tracking the project
    

Explain:

> `.git` is the database where Git stores commits and history.

---

## `git status`

Purpose: **Check repository status**

```bash
git status
```

Shows:

- untracked files
    
- modified files
    
- staged files
    

Example output:

```
Untracked files:
calculator.sh
```

Meaning → Git sees the file but is not tracking it yet.

---

##  `git add`

Purpose: **Add files to staging area**

```bash
git add calculator.sh
```

OR

```bash
git add .
```

Explain:

> This prepares files for the next commit.

Workflow:

```
Edit → git add → git commit
```

---

##  `git commit`

Purpose: **Save a snapshot of the project**

```bash
git commit -m "Add addition feature"
```

Each commit contains:

- changes
    
- timestamp
    
- author
    
- message
    

Explain:

> Commit message should describe **what change was made**.

Example good message:

```
Add subtraction feature
Fix login bug
Update README
```

---

##  `git log`

Purpose: **View commit history**

```bash
git log
```

Compact version:

```bash
git log --oneline
```

Shows:

```
a72f1a Add subtraction feature
b91c2d Initial commit
```

Explain:

> Each commit has a **unique commit ID**.

---

# Branching Concepts

---

##  `git branch`

Purpose: **Create or list branches**

```bash
git branch
```

Create branch:

```bash
git branch feature-login
```

Explain:

> Branch = independent line of development.

Example workflow:

```
main
   │
   └── feature-login
```

---

##  `git checkout`

Purpose: **Switch branches**

```bash
git checkout feature-login
```

Create and switch at once:

```bash
git checkout -b feature-login
```

Explain:

> Developers work on features in separate branches.

---

# Merging

---

##  `git merge`

Purpose: **Combine branches**

Example:

```
main branch
feature branch
```

Merge command:

```bash
git merge feature-division
```

Explain:

> Git combines changes from both branches.

Possible issue:

### Merge Conflict

Occurs when **same line changed in two branches**.

Git shows:

```
<<<<<<< HEAD
code from main
=======
code from feature
>>>>>>> feature
```

Developer must **resolve manually**.

---

# Rebase

---

##  `git rebase`

Purpose: **Move commits to another base**

Example:

Instead of this history:

```
main ----A----B
       \
        C----D
```

Rebase makes it:

```
main ----A----B----C----D
```

Command:

```bash
git rebase main
```

Explain simply:

> Rebase keeps history **clean and linear**.

---

# Temporary Save

---

##  `git stash`

Purpose: **Save unfinished work temporarily**

Example situation:

You edited code but must switch branch.

```
git stash
git checkout main
```

Later restore:

```
git stash pop
```

Explain:

> Stash acts like a temporary shelf.

---

# Undo Changes

---

## `git reset`

Purpose: **Remove commits locally**

```
git reset --hard <commit-id>
```

Explain:

- Deletes commits
    
- Rewrites history
    
- Dangerous for shared repos
    

---

##  `git revert`

Purpose: **Undo commit safely**

```
git revert <commit-id>
```

Git creates a **new commit that reverses the change**.

Explain:

> Use revert for **team projects**.

---

# Tags

---

##  `git tag`

Purpose: **Mark versions**

Example:

```
v1.0
v2.0
v3.0
```

Command:

```bash
git tag v1.0
```

List tags:

```
git tag
```

Explain:

> Tags mark **release versions**.

---

# Remote Repositories

---

##  `git remote`

Purpose: **Connect local repo to GitHub**

Example:

```bash
git remote add origin https://github.com/user/repo.git
```

Now GitHub is called **origin**.

---

## `git push`

Purpose: **Upload commits to GitHub**

```bash
git push origin main
```

Explain:

> Local commits → remote repository.

---

## `git fetch`

Purpose: **Download remote changes only**

```
git fetch origin
```

Does NOT merge.

---

## `git pull`

Purpose: **Fetch + merge**

```
git pull origin main
```

Explain:

```
git pull = git fetch + git merge
```

---

# Fork vs Clone

|Term|Meaning|
|---|---|
|Fork|Copy repo to your GitHub account|
|Clone|Download repo to local machine|

Clone command:

```
git clone <repo-url>
```

---

# Pull Request (PR)

Workflow in teams:

```
1 Create feature branch
2 Make changes
3 Push branch
4 Open Pull Request
5 Code review
6 Merge into main
```

Explain:

> PR is used for **code review before merging**.

---

