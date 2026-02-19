# Discard changes in working directory

git restore <file>

=> Restores the file in the working directory
   to match the staging area (index).
   If the file is not staged, it restores it from the last commit.

# Unstage a file

git restore --staged <file>

=> Removes the file from the staging area
   (keeps the changes in the working directory).

# Restore a file from a specific commit

git restore --source=<commit> <file>

=> Replaces the file in the working directory
   with its version from the specified commit.

# Show file content from a commit

git show <commit>:<file>

=> Prints the content of the file as it was in that commit.

# Old way to discard changes

git checkout <file>

=> Older command that restores the file from the index
   (similar to `git restore <file>`).
   `git restore` is the newer and clearer alternative.

# Revert a commit

git revert <commit>

=> Creates a new commit that undoes the changes
   introduced by the specified commit.
   (It does NOT delete history.)
