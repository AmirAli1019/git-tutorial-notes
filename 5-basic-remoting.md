# Adding a remote
git remote add <remote_name> <url>
=> Adds a new remote repository.
   Example:
   git remote add origin https://github.com/user/repo.git


# Removing a remote
git remote remove <remote_name>
=> Removes the specified remote.


# Changing a remote URL
git remote set-url <remote_name> <new_url>
=> Changes the URL of an existing remote.


# Listing remotes
git remote
=> Shows the list of remote names.

git remote -v
=> Shows remote names along with their URLs.


# Pushing
git push <remote_name> <branch>
=> Pushes the current branch to the specified remote branch.

git push -u <remote_name> <branch>
=> Pushes the branch and sets it as the upstream (tracking) branch.
   After this, you can simply run:
   git push
   git pull


# Pulling
git pull <remote_name> <branch>
=> Fetches and merges changes from the specified remote branch.

git pull -u <remote_name> <branch>
=> Pulls and sets the upstream (tracking) branch.


# Viewing remote branch logs
git log <remote_name>/<branch>
=> Shows the commit history of a remote-tracking branch.
