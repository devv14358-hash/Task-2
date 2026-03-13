

---

# *🚀 Git Cheat Sheet – calculator.sh Example*

---

## *Step 0: Create Project*

bash
mkdir git_calculator
cd git_calculator
vim calculator.sh


Paste initial code:

bash
#!/bin/bash
# Addition
x=1+2


Save and exit :wq!.

---

## *Step 1: Initialize Git Repository*

bash
git init
git status   # check untracked files


---

## *Step 2: Add & Commit Initial Code*

bash
git add calculator.sh
git commit -m "Initial commit - addition feature"
git log --oneline


---

## *Step 3: Make Changes & Commit*

Edit calculator.sh to add subtraction:

bash
#!/bin/bash
# Addition
x=1+2

# Subtraction
y=2-1


bash
git status
git diff          # see changes
git add calculator.sh
git commit -m "Add subtraction feature"


---

## *Step 4: Create Feature Branch*

bash
git checkout -b feature-division


Add division:

bash
#!/bin/bash
# Addition
x=1+2

# Subtraction
y=2-1

# Division
d=10/2


bash
git add calculator.sh
git commit -m "Add division feature"
git log --oneline


---

## *Step 5: Switch Branches*

bash
git checkout main
git log --oneline   # division not in main yet


---

## *Step 6: Merge Branch*

bash
git merge feature-division


✅ If merge conflict appears:

text
<<<<<<< HEAD
# main code
=======
# feature code
>>>>>>> feature-division


Fix manually, then:

bash
git add calculator.sh
git commit -m "Fix merge conflict"


---

## *Step 7: Rebase Example*

bash
git checkout -b feature-percentage


Edit calculator.sh:

bash
# Percentage
p=50*2/100


bash
git add calculator.sh
git commit -m "Add percentage feature"
git checkout main
git rebase feature-percentage
# if conflict, fix file, then:
git add calculator.sh
git rebase --continue


---

## *Step 8: Stash Unfinished Work*

bash
vim calculator.sh
# Modulus function m=10%3

git stash             # save changes temporarily
git checkout main     # switch branch safely
git stash pop         # bring changes back


---

## *Step 9: Reset vs Revert*

bash
# Reset (remove commits locally, changes history)
git reset --hard <commit-id>

# Revert (safe for shared repo, adds new commit to undo changes)
git revert <commit-id>


---

## *Step 10: Tags for Releases*

bash
git tag v1.0             # mark release version
git tag                  # list tags
git push origin v1.0     # push tag to remote


---

## *Step 11: Pull vs Fetch*

bash
git fetch origin          # download remote changes, do not merge
git pull origin main      # download + merge remote changes


---

## *Step 12: Remote Repo Setup*

bash
git remote add origin https://github.com/username/git_calculator.git
git push -u origin main


* *Fork* → copy repo to your GitHub account
* *Clone* → download repo to local machine

---

## *Step 13: Pull Request (PR) Workflow*

1️⃣ Create feature branch:

bash
git checkout -b feature-multiplication


2️⃣ Edit file:

bash
# Multiplication
m=2*5


3️⃣ Commit & push:

bash
git add calculator.sh
git commit -m "Add multiplication feature"
git push origin feature-multiplication


4️⃣ Go to GitHub → Create Pull Request
5️⃣ Team reviews → Merge into main

---

## *Step 14: Quick Branch Strategy*

| Branch      | Purpose                |
| ----------- | ---------------------- |
| main/master | always updated, stable |
| feature     | new development        |
| release     | tested & shipped       |
| hotfix      | urgent bug fix         |

---

## *Step 15: Quick Git Commands Summary*

bash
git init          # initialize repo
git clone         # download repo
git status        # check file status
git add           # stage changes
git commit        # save changes
git push          # push to remote
git pull          # fetch + merge remote changes
git branch        # list/create branches
git checkout      # switch branches
git merge         # merge branch into current
git rebase        # linearize commits
git log           # view commit history
git diff          # show changes
git stash         # save unfinished work
git tag           # mark release version


---

✅ *All concepts included:*

* merge conflicts
* pull vs fetch
* reset vs revert
* stash
* tags
* PR workflow
