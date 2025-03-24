objectives

Simulate an advanced Git scenario that includes forced pushes, recovering lost commits, 
and a multi-branch workflow.

================================================================

steps followed

>> created a file in main branch named test.js
>> created a brach named feature and then checked out it
>>  created a file in main branch named test.js
>> created two commits and squashed it
>> pushed it to remote repository
>> again dit the same 
>> pushed it to remote repository
>> but failed and used "git push origin main --force"
>> it pushed 
>> now lost the commit "fe7f647" in squashing
>> i have used reflog it displayed all the commits
>> checkedout to that commit
>> created a new brach and checkced out to it and all changes are reflected there

==> so the reflog helps if a  force pusg erases a commit by other person on a same brach we can recover it so it is a 
life saver in bug fix times and in a collaborative workflow.

==> if brach is not shared we can use force push after a rebase 
==> if brach is shared, we should not use force push


===> Insted we can use "git pull origin shared  --rebase" . it is safe .