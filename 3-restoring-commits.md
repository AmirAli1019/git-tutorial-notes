git restore "<file>" ==> Discards specified file changes in working directory based on the latest commit.
git restore --staged "<file>" ==> Unstages the file or directory.
git restore --source="<commit hash>" "<file_name>" ==> Replaces the file with an older version from the specified commit.

git show "<commit_hash>":"<file_name>" ==> Prints the content of the file during the specified commit.

git checkout "<file>" ==> Similar to `git restore "<file>"`

git revert "<commit hash>" ==> Does the opposite of the actions we done in the specified commit. For example if we had created a file it deletes just the same file.
