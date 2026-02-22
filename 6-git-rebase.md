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

**A word of caution:**

Only rebase branches that you are working on alone. If you rebase a branch that others are using, it can scramble their history and cause a bit of a headache!

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
