objectives

-->Use interactive rebase to tidy up your commit history.

==================================================================================================================

Steps followed for Editing commit messages

--> created learnings.txt and commited with a typo "learnins.txt" 
--> used "git rebase -i HEAD~1 " it will list last commit
--> Opened vim editor and changed "pick" command to "reword" 
--> again it Opened interactive rebase editor and there i have changed the message to "learnings.txt"
--> saved it and  exited.

output 

>>> git rebase -i HEAD~1

[detached HEAD 3e7e2c0] created learnings.txt
 Date: Wed Mar 19 16:10:48 2025 +0530
 1 file changed, 1 insertion(+)
 create mode 100644 Task5/learnings.txt
Successfully rebased and updated refs/heads/main.


