# List branches

git branch
=> Lists all local branches.
   The current active branch is marked with *.

git branch -v
=> Lists local branches along with
   the latest commit hash and message.

# Create a branch

git branch <branch_name>
=> Creates a new branch.
   (Does NOT switch to it.)

# Delete a branch

git branch -d <branch_name>
=> Deletes the branch if it has been fully merged.

git branch -D <branch_name>
=> Force deletes the branch
   (even if it contains unmerged commits).

# Switch branches (old command)

git checkout <branch_name>
=> Switches to the specified branch.

# Create and switch

git checkout -b <branch_name>
=> Creates a new branch and switches to it.

# Merge branches

git merge <branch_name>
=> Merges the specified branch
   into the current active branch.
