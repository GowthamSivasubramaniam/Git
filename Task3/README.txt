commit 4ca4bf8980ab9853adf000927482a5932aba2199 (HEAD -> main)
Author: GowthamSivasubramaniam <gowthamsivasubramaniam03@gmail.com>
Date:   Wed Mar 19 11:11:05 2025 +0530

    created README file and undo file

now have make the file unstaged after staging 
for that the command is git restore --staged "filename" 

output


git status          
On branch main
Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        modified:   undo.txt

git restore --staged undo.txt
git status                    
On branch main
Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        modified:   undo.txt

no changes added to commit (use "git add" and/or "git commit -a")

git checkout undo.txt  
Updated 1 path from the index



seeing commit revert