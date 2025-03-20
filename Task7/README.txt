objectives

===> Selectively apply a commit from one branch to another using cherry-pick.
=================================================================================================================
Steps to be followed 

==> created a README file in "main branch"
==> commited it.
==> checkck out to "test branch"
==> added contents to README file.
==> commited it.
==> created a file in Test branch as "test.txt"
==> commited it.
==> Did cherry pick ====> "git cherry-pick 3eb13da"
==> got conflict and resolved it and staged it.
==> Then executed "git cherry-pick --continue"
==> created a commit message "updated Readme.txt took a commit from test branch using cherry pick and resolved it".

output of git log

>> 2253d63 (HEAD -> main) updated Readme.txt took a commit from test branch using cherry pick and resolved it
>> 78ea327 Updated Readme.txt
>> 48d41ec (origin/main) Created updated README.txt
>> baf58bf Created and updated objectives.txt and stashed them
>> 396f669 Updated README.txt
>> 2cf52a1 Updated README.txt

The cherry picked one is present!

