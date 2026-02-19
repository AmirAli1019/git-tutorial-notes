git config user.name "<Your Name>"
git config user.email "<Your Email>"
git config core.editor "<Your Desired Editor>" ==> Changes the default text editor for git.
For the above commands add --global to apply changes globally for all further repositories.

git init ==> To initialize a new repository.

git add file_1 file_2 ... (or some directories) => To stage changed files.
git add -A ==> To stage everything that can be staged in the current repository.
git add -p ==> Stages changes in an interactive way.

git commit ==> To commit changes
git commit -a ==> To auto stage all `tracked` files and then commit them. (No `git add` needed).
git commit -m "<commit message>" -m ...
git commit --amend ==> Replaces the latest commit by creating a new commit.

git status ==> shows the status of the repository.

git show "<commit hash>" ==> shows the commit changes details.

git log ==> Shows the log of the repository.
git log -p ==> Displays the changes (diffings) alongside the commits.
git log -3 ==> Displays just the last 3 commits.

git log --graph ==> Draw a text-based graphical representation of the commit history on the left hand side of the output.
git log --oneline ==> the commit message is prefixed with this information on the same line.
You can combine them together:
git log --graph --oneline

git diff ==> Displays the difference between the latest commit and current `unstaged` repository files.
git diff --staged ==> Displays the differences between the latest commit and current `staged` repository files.
git diff "<commit hash>" ==> Displays the differences between the specified commit and current `staged` or `unstaged` repository files.
git diff "<commit hash1>" "<commit hash2>" ==> Displays the differences between two specified commit.

git rm "<file_name>" ==> Removes a file from the repository and stages the change automatically (ready to commit).
git mv "<file_name>" ==> Moves a file in the repository and stages the change automatically (ready to commit).
