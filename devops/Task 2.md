Below is a **complete Git calculator practice project** that covers **all important local Git concepts**:
These are the git commands we have seen so far in the class

- init
    
- add
    
- commit
    
- status
    
- diff
    
- log
    
- branching
    
- merge
    
- merge conflict
    
- rebase
    
- stash
    
- reset
    
- revert
    
- tags
    

It uses **4 branches** so students clearly see the workflow.

This works **very well for a 2-hour class**.

---

# Git Calculator Project (Complete Local Git Practice)

## Project Structure

```bash
git_calculator/
 └── calculator.sh
```

---

# Step 0 — Create Project

```bash
mkdir git_calculator
cd git_calculator
vim calculator.sh
```

Add code:

```bash
#!/bin/bash

echo "Simple Calculator"

a=10
b=5

echo "Addition: $((a+b))"
```

Save.

---

# Step 1 — Initialize Git

```bash
git init
```

Check status:

```bash
git status
```

Output shows:

```
calculator.sh is untracked
```

---

# Step 2 — First Commit

Stage file:

```bash
git add calculator.sh
```

Commit:

```bash
git commit -m "Initial calculator with addition"
```

View history:

```bash
git log --oneline
```

---

# Step 3 — Modify Code (Subtraction)

Edit file:

```bash
vim calculator.sh
```

Update:

```bash
#!/bin/bash

echo "Simple Calculator"

a=10
b=5

echo "Addition: $((a+b))"
echo "Subtraction: $((a-b))"
```

Check change:

```bash
git diff
```

Commit:

```bash
git add calculator.sh
git commit -m "Add subtraction feature"
```

---

# Step 4 — Create Branch (Multiplication)

Create branch:

```bash
git checkout -b feature-multiplication
```

Edit file:

```bash
echo "Multiplication: $((a*b))"
```

File becomes:

```bash
#!/bin/bash

echo "Simple Calculator"

a=10
b=5

echo "Addition: $((a+b))"
echo "Subtraction: $((a-b))"
echo "Multiplication: $((a*b))"
```

Commit:

```bash
git add calculator.sh
git commit -m "Add multiplication feature"
```

Check branches:

```bash
git branch
```

---

# Step 5 — Create Another Branch (Division)

Switch back to main:

```bash
git checkout main
```

Create new branch:

```bash
git checkout -b feature-division
```

Edit:

```bash
echo "Division: $((a/b))"
```

File:

```bash
#!/bin/bash

echo "Simple Calculator"

a=10
b=5

echo "Addition: $((a+b))"
echo "Subtraction: $((a-b))"
echo "Division: $((a/b))"
```

Commit:

```bash
git add calculator.sh
git commit -m "Add division feature"
```

---

# Step 6 — Merge Branch

Switch to main:

```bash
git checkout main
```

Merge multiplication:

```bash
git merge feature-multiplication
```

Now merge division:

```bash
git merge feature-division
```
merge conflict came here 











View history:

```bash
git log --oneline --graph
```

Students see **branch merge graph**.

---

# Step 7 — Create Conflict Branch

Create new branch:

```bash
git checkout -b feature-percentage
```

Edit file:

```bash
echo "Percentage: $((a*b/100))"
```

Commit:

```bash
git add calculator.sh
git commit -m "Add percentage feature"
```

---

Now create conflict.

Switch to main:

```bash
git checkout main
```

Edit same line:

```bash
echo "Addition Result: $((a+b))"
```

Commit:

```bash
git add calculator.sh
git commit -m "Modify addition output"
```

---

# Step 8 — Merge Conflict

Merge branch:

```bash
git merge feature-percentage
```

Git shows conflict like:

```
<<<<<<< HEAD
echo "Addition Result: $((a+b))"
=======
echo "Percentage: $((a*b/100))"
>>>>>>> feature-percentage
```

Fix manually:

```bash
echo "Addition Result: $((a+b))"
echo "Percentage: $((a*b/100))"
```

Commit fix:

```bash
git add calculator.sh
git commit -m "Resolve merge conflict"
```

---

# Step 9 — Rebase Example

Create branch:

```bash
git checkout -b feature-modulus
```

Add:

```bash
echo "Modulus: $((a%b))"
```

Commit:

```bash
git add calculator.sh
git commit -m "Add modulus feature"
```

Rebase onto main:

```bash
git checkout main
git rebase feature-modulus
```

Students see **clean history**.

---

# Step 10 — Stash Example

Edit file but don't commit:

```bash
echo "Square: $((a*a))"
```

Check status:

```bash
git status
```

Stash changes:

```bash
git stash
```

Switch branch safely:

```bash
git checkout feature-division
```

Bring changes back:

```bash
git stash pop,conflict came here too 
```

---

# Step 11 — Reset Example

View commits:

```bash
git log --oneline
```

Reset to previous commit:

```bash
git reset --hard HEAD~1
```

This **removes the last commit**.

---

# Step 12 — Revert Example

Undo commit safely:

```bash
git revert HEAD
```

Git creates **new commit reversing change**.

---

# Step 13 — Tag Release

Mark version:

```bash
git tag v1.0
```

List tags:

```bash
git tag
```

---

# Final Calculator Code

After all merges:

```bash
#!/bin/bash

echo "Simple Calculator"

a=10
b=5

echo "Addition: $((a+b))"
echo "Subtraction: $((a-b))"
echo "Multiplication: $((a*b))"
echo "Division: $((a/b))"
echo "Addition Result: $((a+b))" 

echo "Percentage: $((a*b/100))"
echo "Modulus: $((a%b))"
```

---

# Final Branch Structure

Students will have:

```
main
feature-multiplication
feature-division
feature-percentage
feature-modulus
```

---

# Git Concepts Covered

|Concept|Where Students Learn|
|---|---|
|init|repo creation|
|status|tracking changes|
|add|staging|
|commit|saving history|
|diff|viewing code changes|
|log|commit history|
|branch|feature development|
|merge|combining branches|
|conflict|resolving conflicts|
|rebase|clean history|
|stash|temporary save|
|reset|delete commit|
|revert|safe undo|
|tag|version marking|

---
