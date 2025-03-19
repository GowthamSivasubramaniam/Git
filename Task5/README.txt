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

==================================================================================================================

Steps followed for Squashing commit messages

--> updated learnings.txt and commited with "Updated Learnings.txt"
--> used "git rebase -i HEAD~3 " it will list last 3 commits
--> Opened vim editor and changed "pick" command to "Squash"
--> again it Opened interactive rebase editor and there have created another  message to "Squashing 3 commits"
--> saved it and  exited.

output git rebase -i HEAD~3
>>>
# This is a combination of 3 commits.
# This is the 1st commit message:

created learnings.txt

# This is the commit message #2:

Created README.txt

# This is the commit message #3:

Updated Learnings.txt

commit 91ffdbf12252f47e870bcc4ae53b7bdb9b97bc3f (HEAD -> main)
Author: GowthamSivasubramaniam <gowthamsivasubramaniam03@gmail.com>
Date:   Wed Mar 19 16:10:48 2025 +0530

    created learnings.txt
    
    Created README.txt
    
    Updated Learnings.txt
    
    Squashing 3 commits

==================================================================================================================

Steps followed for reordering commit messages

--> updated learnings.txt and commited with "Updated learnings.txt for first commit for reordering purpose"
--> updated learnings.txt and commited with "Updated learnings.txt for second commit for reordering purpose"
--> updated learnings.txt and commited with "Updated learnings.txt for third commit for reordering purpose"
--> used "git rebase -i HEAD~3 " it will list last 3 commits
--> Opened vim editor and changed "pick" command to "Squash"
--> again it Opened interactive rebase editor and there have created another  message to "Squashing 3 commits"
--> saved it and  exited.

output before reordering for git log command


=====> 67a3c5f (HEAD -> main) Updated learnings.txt for third commit for reordering purpose
=====> ec62cf5 Updated learnings.txt for second commit for reordering purpose
=====> 154a162 Updated learnings.txt for first commit for reordering purpose