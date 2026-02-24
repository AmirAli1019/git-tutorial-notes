Think of `git rebase` as a way to "rewrite history" so your project timeline stays clean and linear.

Instead of merging two branches together (which creates a "knot" in your timeline), rebasing takes the work you did on your branch and moves it to the very tip of the main branch.

**How it works:**

1. Git finds the point where your branch originally split off from the main line.

2. It temporarily "lifts" your new commits off to the side.

3. It adds all the latest updates from the main branch to your project.

4. It "puts" your commits back on top, one by one.

**Why use it?**

- Cleanliness: Your history looks like a straight line instead of a tangled web of merge lines.

- Up-to-date: It makes it look like you started your work after everyone else finished theirs, avoiding messy conflicts later.

---

To rebase a branch go to your feature branch and tell git to "rebase" it to the main branch:

`git checkout <branch>`

`git rebase main`

This action may fails because of some conflicts between two branches. Solve them and to continue rebasing:

`git rebase --continue`

Or if you want to abort that:

`git rebase --abort`

If the remote reject pushing after rebase you should force push it:

`git push --force`

---

Force pushing is not recommended on branches that you work on as a team, as it alters the project's history and can cause difficulties when pulling changes.

However, there are several ways to address this issue after a force push:

1. The "Clean History" Way (Rebase)

    This is usually the preferred method if you want a linear history. It takes your local commits and "re-stacks" them on top of the new remote commits.

`git pull --rebase`

2. The "Standard" Way (Merge)

    This creates a new "merge commit" that ties your local work and the remote work together. It’s visible in the logs that a merge happened.

`git pull --no-rebase`

3. The "Reset" Way (Overwrite Local)

    Warning: This deletes any local changes you haven't pushed. If you don't care about your local commits and just want your folder to match GitHub exactly:

`git reset --hard origin/main`
