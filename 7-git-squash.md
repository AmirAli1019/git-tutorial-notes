Squashing in Git is the process of taking several small commits and condensing them into a single, clean commit. This is standard practice before merging a feature branch into `main` to keep the history readable.

The most common and flexible way to do this is using an **Interactive Rebase**.

---

### Step 1: Start the Interactive Rebase

You need to tell Git how far back you want to go. If you want to squash the last **3** commits, run:

```bash
git rebase -i HEAD~3
```

### Step 2: Choose Which Commits to Squash

Your default text editor (usually Vim or Nano) will open with a list of commits that looks like this:

```text
pick a1b2c3d My first commit
pick e4f5g6h My second commit
pick i7j8k9l My third commit
```

To squash them, keep the **top** commit as `pick` and change the others to `squash` (or just `s`):

```text
pick a1b2c3d My first commit
s e4f5g6h My second commit
s i7j8k9l My third commit
```

**Save and close the editor.**

### Step 3: Rewrite the Commit Message

After saving, Git will open a second window showing the commit messages from all the squashed commits.

1. Delete the messages you don't want.
2. Type a new, clean message for the combined commit.
3. Save and close.

### Step 4: Push the Changes

Since you have rewritten history, a normal `git push` will be rejected. You must force push:

```bash
git push --force
```

*(Use `--force-with-lease` if you want to be safer; it prevents you from accidentally overwriting a teammate's work if they pushed something while you were rebasing.)*

---

### Alternative: Squashing via Merge

If you are finished with a branch and just want to merge it into `main` as one single commit without doing the manual rebase dance:

```bash
git checkout main
git merge --squash feature-branch
git commit -m "Your final clean commit message"
```

### Summary of Commands

| Method | Use Case |
| --- | --- |
| `rebase -i` | Best for cleaning up your own local branch before anyone else sees it. |
| `merge --squash` | Best for moving a whole branch into `main` as one unit. |
