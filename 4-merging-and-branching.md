git branch ==> Displays the name of the current active branch and also the other branches.
git branch -v ==> Displays the latest commits details alongside the names of the existing branches.
git branch "<branch_name>" ==> Creates a new branch.

git branch -d "<branch_name>" ==> To delete a branch.
git branch -D "<branch_name>" ==> If you have some unmerged commits in the branch to force delete it use this command.

git checkout "<branch_name>" ==> Changes the active branch to the specified one.
git checkout -b "<branch_name>" ==> Creates a new branch and automatically switches to that.

git merge "<branch_name>" ==> Merges the specified branch to the current active branch.
