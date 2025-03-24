output


commit 4ca4bf8980ab9853adf000927482a5932aba2199 (HEAD -> main)
Author: GowthamSivasubramaniam <gowthamsivasubramaniam03@gmail.com>
Date:   Wed Mar 19 11:11:05 2025 +0530

    created README file and undo file

---> Now have make the file unstaged after staging 
---> for that the command is git restore --staged "filename" 






_________________________________________________________________



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



_________________________________________________________________




output for git revert 60d3c14c7196938d977599cbae587110e2b869b9

Revert " simulating revert command"

-->This reverts commit 60d3c14c7196938d977599cbae587110e2b869b9.


--> The git revert undos the commit but keeps the history same without altering

--> The git restore --soft will make the changes  staged and alters the history and changes head 
position to the given commit hash

--> The git restore --mixed will make the changes  unstaged and alters the 
history and changes head position to the given commit hash

--> The git restore --hard will change the content of that commit hash and the changes done after that 
commit hash will be removed and alters the history and changes head position to the given
commit hash .


output 



gowtham@Gowthams-MacBook-Pro Task3 % git reset --soft d2757eaf64517925459d22b95f66d84b6ae102b2                                         
gowtham@Gowthams-MacBook-Pro Task3 % git log                                                  
commit d2757eaf64517925459d22b95f66d84b6ae102b2 (HEAD -> main)
Author: GowthamSivasubramaniam <gowthamsivasubramaniam03@gmail.com>
Date:   Wed Mar 19 12:21:13 2025 +0530

    completed revert

commit 60d3c14c7196938d977599cbae587110e2b869b9
Author: GowthamSivasubramaniam <gowthamsivasubramaniam03@gmail.com>
Date:   Wed Mar 19 12:04:55 2025 +0530

     simulating revert command

commit fea27c2e0a32fea7f5228ea2c15a5541621a532f
Author: GowthamSivasubramaniam <gowthamsivasubramaniam03@gmail.com>
Date:   Wed Mar 19 11:57:10 2025 +0530

    Updated README.txt with undoing procedure for staged files

commit 2fddebbce9fa8f7f534dfa65b24c6742439ec079
Author: GowthamSivasubramaniam <gowthamsivasubramaniam03@gmail.com>
Date:   Wed Mar 19 11:19:43 2025 +0530
gowtham@Gowthams-MacBook-Pro Task3 % git reset --soft d2757eaf64517925459d22b95f66d84b6ae102b2
gowtham@Gowthams-MacBook-Pro Task3 % git reset --mixed d2757eaf64517925459d22b95f66d84b6ae102b2
gowtham@Gowthams-MacBook-Pro Task3 % git reset --mixed 60d3c14c7196938d977599cbae587110e2b869b9
Unstaged changes after reset:
M       Task3/README.txt
gowtham@Gowthams-MacBook-Pro Task3 % git log                                                   
commit 60d3c14c7196938d977599cbae587110e2b869b9 (HEAD -> main)
Author: GowthamSivasubramaniam <gowthamsivasubramaniam03@gmail.com>
Date:   Wed Mar 19 12:04:55 2025 +0530

     simulating revert command

commit fea27c2e0a32fea7f5228ea2c15a5541621a532f
Author: GowthamSivasubramaniam <gowthamsivasubramaniam03@gmail.com>
Date:   Wed Mar 19 11:57:10 2025 +0530

    Updated README.txt with undoing procedure for staged files

commit 2fddebbce9fa8f7f534dfa65b24c6742439ec079
Author: GowthamSivasubramaniam <gowthamsivasubramaniam03@gmail.com>
Date:   Wed Mar 19 11:19:43 2025 +0530

    changed undo.txt

commit 075f3103d50b443c9377eefe3203cb848fafd157
Author: GowthamSivasubramaniam <gowthamsivasubramaniam03@gmail.com>
Date:   Wed Mar 19 11:13:58 2025 +0530
gowtham@Gowthams-MacBook-Pro Task3 % git reset --soft d2757eaf64517925459d22b95f66d84b6ae102b2 
gowtham@Gowthams-MacBook-Pro Task3 % git commit -m "completed revert"                          
[main 6d0a581] completed revert
 1 file changed, 1 insertion(+), 6 deletions(-)
gowtham@Gowthams-MacBook-Pro Task3 % git add .
gowtham@Gowthams-MacBook-Pro Task3 % git commit -m "completed revert"
[main 92d5343] completed revert
 1 file changed, 6 insertions(+), 1 deletion(-)
gowtham@Gowthams-MacBook-Pro Task3 % git reset --hard d2757eaf64517925459d22b95f66d84b6ae102b2
HEAD is now at d2757ea completed revert
gowtham@Gowthams-MacBook-Pro Task3 % git log                                                  
commit d2757eaf64517925459d22b95f66d84b6ae102b2 (HEAD -> main)
Author: GowthamSivasubramaniam <gowthamsivasubramaniam03@gmail.com>
Date:   Wed Mar 19 12:21:13 2025 +0530

    completed revert

commit 60d3c14c7196938d977599cbae587110e2b869b9
Author: GowthamSivasubramaniam <gowthamsivasubramaniam03@gmail.com>
Date:   Wed Mar 19 12:04:55 2025 +0530

     simulating revert command

commit fea27c2e0a32fea7f5228ea2c15a5541621a532f
Author: GowthamSivasubramaniam <gowthamsivasubramaniam03@gmail.com>
Date:   Wed Mar 19 11:57:10 2025 +0530

    Updated README.txt with undoing procedure for staged files

commit 2fddebbce9fa8f7f534dfa65b24c6742439ec079
Author: GowthamSivasubramaniam <gowthamsivasubramaniam03@gmail.com>
Date:   Wed Mar 19 11:19:43 2025 +0530
gowtham@Gowthams-MacBook-Pro Task3 % git reset --hard 60d3c14c7196938d977599cbae587110e2b869b9
HEAD is now at 60d3c14  simulating revert command
gowtham@Gowthams-MacBook-Pro Task3 % git log                                                  
commit 60d3c14c7196938d977599cbae587110e2b869b9 (HEAD -> main)
Author: GowthamSivasubramaniam <gowthamsivasubramaniam03@gmail.com>
Date:   Wed Mar 19 12:04:55 2025 +0530

     simulating revert command

commit fea27c2e0a32fea7f5228ea2c15a5541621a532f
Author: GowthamSivasubramaniam <gowthamsivasubramaniam03@gmail.com>
Date:   Wed Mar 19 11:57:10 2025 +0530

    Updated README.txt with undoing procedure for staged files

commit 2fddebbce9fa8f7f534dfa65b24c6742439ec079
Author: GowthamSivasubramaniam <gowthamsivasubramaniam03@gmail.com>
Date:   Wed Mar 19 11:19:43 2025 +0530

    changed undo.txt

commit 075f3103d50b443c9377eefe3203cb848fafd157
Author: GowthamSivasubramaniam <gowthamsivasubramaniam03@gmail.com>
Date:   Wed Mar 19 11:13:58 2025 +0530
gowtham@Gowthams-MacBook-Pro Task3 % git reset --hard d2757eaf64517925459d22b95f66d84b6ae102b2
HEAD is now at d2757ea completed revert
gowtham@Gowthams-MacBook-Pro Task3 % git reset --soft d2757eaf64517925459d22b95f66d84b6ae102b2
gowtham@Gowthams-MacBook-Pro Task3 % git reset --hard d2757eaf64517925459d22b95f66d84b6ae102b2
HEAD is now at d2757ea completed revert