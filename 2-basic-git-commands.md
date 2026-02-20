# Configuration

`git config user.name "<Your Name>"`

`git config user.email "<Your Email>"`

`git config core.editor "<Your Desired Editor>"`

=> Sets configuration values for Git.

   Add --global to apply them globally (for all repositories on your system).

   Without --global, the settings apply only to the current repository.

# Initialize a repository

`git init`

=> Creates a new Git repository in the current directory.

# Staging

`git add file1 file2 ...`

=> Stages specific files or directories.

`git add -A`

=> Stages all changes (new, modified, and deleted files).

`git add -p`

=> Interactively stages parts of changes (hunks).

# Committing

`git commit`

=> Creates a commit from staged changes.

`git commit -a`

=> Automatically stages all modified tracked files and commits them.

   (Does NOT include untracked files.)

`git commit -m "message"`

=> Creates a commit with a message.

`git commit --amend`

=> Replaces the most recent commit with a new one.

   (Useful for fixing the commit message or adding forgotten changes.)

# Status

`git status`

=> Shows the current state of the working directory and staging area.

# Viewing commits

`git show <commit-hash>`

=> Shows detailed information and changes of a specific commit.

`git log`

=> Shows commit history.

`git log -p`

=> Shows commit history with diffs.

`git log -n 3`

=> Shows the last 3 commits.

`git log --graph`

=> Displays a text-based graph of branch history.

`git log --oneline`

=> Shows each commit on a single line (short hash + message).

`git log --all`

=> Displays the commit history of all branches, tags, and remote-tracking refs in the repository, rather than just the current branch.

# Combine options

`git log --graph --oneline --all`

# Differences

`git diff`

=> Shows differences between the working directory and the staging area.

   (Unstaged changes)

`git diff --staged`

=> Shows differences between the staging area and the last commit.

   (Staged changes)

`git diff <commit>`

=> Shows differences between the specified commit and the working directory.

`git diff <commit1> <commit2>`

=> Shows differences between two commits.

# Removing and moving files

`git rm <file>`

=> Removes the file and stages the deletion.

`git mv <old_name> <new_name>`

=> Renames or moves a file and stages the change.
