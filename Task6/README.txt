Objective 

==> Learn how to use Git stash to save uncommitted work temporarily.

================================================================================================================

Steps done 

==> First created a file named objectives.txt
==> Done made some changes and commited it.
==> Again changed the objectives.txt and applied "git stash" but if done without staging it shows it as untracked.
==> want stash untracked  also can go with  "git stash --all".
==> or for specific file alone can go with "git stash push --filename" 
==> i did the same "git stash push --objectives.txt.
==> switched to test branch and did some commits like created a file called "test.txt" and commited it.
==> returned back to main branch and poped my stash with "git stash pop"
==> again did changes to  objectives.txt and viewed my stash with "git stash list or git stash show "
==> and removed stash with git stash drop stash@{0}.


output

>>> git stash push --keep-index -- objectives.txt 
Saved working directory and index state WIP on main: bbaae3d Completed Task5 and updated README.txt
    
>>> git stash show
 Task6/objectives.txt | 1 +
 1 file changed, 1 insertion(+)
>>>  git checkout test
Switched to branch 'test'
>>> touch test.txt
>>> git add .  
>>> git commit -m "commiting test"
[test 98fece8] commiting test
 2 files changed, 1 insertion(+)
 create mode 100644 Task6/objectives.txt
 create mode 100644 Task6/test.txt
>>> git checkout main             
Switched to branch 'main'
>>> git stash show 
 Task6/objectives.txt | 1 +
 1 file changed, 1 insertion(+)
>>> git stash pop
On branch main
Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        new file:   objectives.txt

Dropped refs/stash@{0} (eb416cd56612e88cb284c4625e0982389affada8)
>>> git stash push
Saved working directory and index state WIP on main: bbaae3d Completed Task5 and updated README.txt
>>> git stash list
stash@{0}: WIP on main: bbaae3d Completed Task5 and updated README.txt
>>> git stash drop stash@{0}
Dropped stash@{0} (ea9a9a1e3f72530bbf34bcd40592e0b5d03deeb7)