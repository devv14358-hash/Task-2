DEV@DESKTOP-IL3NP67 MINGW64 ~/git_calculator (master)
$ git merge feature-division
Auto-merging calculator.sh
CONFLICT (content): Merge conflict in calculator.sh
Automatic merge failed; fix conflicts and then commit the result.

DEV@DESKTOP-IL3NP67 MINGW64 ~/git_calculator (master|MERGING)
$ cat calculator.sh
#!/bin/bash

echo "Simple Calculator"

a=10
b=5

echo "Addition: $((a+b))"
echo "Subtraction: $((a-b))"
<<<<<<< HEAD
echo "Multiplication: $((a*b))"
=======
echo "Division: $((a/b))"
>>>>>>> feature-division

DEV@DESKTOP-IL3NP67 MINGW64 ~/git_calculator (master|MERGING)
$ vim calculator.sh

DEV@DESKTOP-IL3NP67 MINGW64 ~/git_calculator (master|MERGING)
$ git status
On branch master
You have unmerged paths.
  (fix conflicts and run "git commit")
  (use "git merge --abort" to abort the merge)

Unmerged paths:
  (use "git add <file>..." to mark resolution)
        both modified:   calculator.sh

no changes added to commit (use "git add" and/or "git commit -a")

DEV@DESKTOP-IL3NP67 MINGW64 ~/git_calculator (master|MERGING)
$ git commit -am "fixed merge division"
[master 1d5e964] fixed merge division

DEV@DESKTOP-IL3NP67 MINGW64 ~/git_calculator (master)
$ cat calculator.sh
#!/bin/bash

echo "Simple Calculator"

a=10
b=5

echo "Addition: $((a+b))"
echo "Subtraction: $((a-b))"
echo "Multiplication: $((a*b))"
echo "Division: $((a/b))"


DEV@DESKTOP-IL3NP67 MINGW64 ~/git_calculator (master)



GIT STASH ERROR 

DEV@DESKTOP-IL3NP67 MINGW64 ~/git_calculator (master)
$ git stash
Saved working directory and index state WIP on master: c01daaa Add modulus feature

DEV@DESKTOP-IL3NP67 MINGW64 ~/git_calculator (master)
$ git checkout feature-division
Switched to branch 'feature-division'

DEV@DESKTOP-IL3NP67 MINGW64 ~/git_calculator (feature-division)
$ git stash pop
Auto-merging calculator.sh
CONFLICT (content): Merge conflict in calculator.sh
On branch feature-division
Unmerged paths:
  (use "git restore --staged <file>..." to unstage)
  (use "git add <file>..." to mark resolution)
        both modified:   calculator.sh

no changes added to commit (use "git add" and/or "git commit -a")
The stash entry is kept in case you need it again.

DEV@DESKTOP-IL3NP67 MINGW64 ~/git_calculator (feature-division)
$ vim calculator.sh

DEV@DESKTOP-IL3NP67 MINGW64 ~/git_calculator (feature-division)
$ git status
On branch feature-division
Unmerged paths:
  (use "git restore --staged <file>..." to unstage)
  (use "git add <file>..." to mark resolution)
        both modified:   calculator.sh

no changes added to commit (use "git add" and/or "git commit -a")

DEV@DESKTOP-IL3NP67 MINGW64 ~/git_calculator (feature-division)
$ git add .

DEV@DESKTOP-IL3NP67 MINGW64 ~/git_calculator (feature-division)
$ git commit -m "stash merge handled"
[feature-division 80d3da9] stash merge handled
 1 file changed, 5 insertions(+)

DEV@DESKTOP-IL3NP67 MINGW64 ~/git_calculator (feature-division)
$ git status
On branch feature-division
nothing to commit, working tree clean

DEV@DESKTOP-IL3NP67 MINGW64 ~/git_calculator (feature-division)
$
