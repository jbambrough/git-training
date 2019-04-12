# git-training

Sandbox repository for Git Training

## What is this?

This repository is a sandbox project for learning and improving Git techniques

## Prequisites

- Basic understanding of Git commands
- Have Git installed on your local machine
- Have Visual Studio Code installed
- Have Node.js installed

## Terminology

- `local` - your laptop
- `remote` - server where the repository is stored
- `tracked / untracked` - file/blob is _"tracked"_ by Git (untracked is a file that has never been committed)
- `stage` - mark change to be committed (if you make additional changes after changing, you must again stage the newer changes)
- `modified` - a tracked file that has been modified from the last revision
- `branch` - working copy of code, typically used when you are creating a new feature or fixing a bug
- `HEAD` - special pointer that refers to the _latest commit_ of the checked out branch
- `SHA1 hash` - example: f4f78b319c308600eab015a5d6529add21660dc1. SHA1 hash generated from the delta of the commit.
- `Pull Request (PR)` - This is a GitHub-only concept, which refers to a pending merge on the remote which can be reviewed before merging remotely.
- `Merge Conflict` - When merging, Git failed to automatically resolve the delta of the branches being merged, which requires human intervention
- `rebase` - replays a set of commits on top of a specific base commit
- `interactive rebase` - a rebase that allows you to control how the changes are replayed

## Common Commands

- `git clone` - copy repository down to your local
- `git fetch` - get changes from remote
- `git pull` - fetch plus merge
- `git push` - put your local committed changes to the remote
- `git reset` - tool for undoing changes
- `git diff` - show changes between commits
- `git revert` - show changes between commits
- `git stash` - temporarily store your working code
- `git merge` - apply all unique commits from branch A into branch B in one commit with final result
- `git rebase` - gets all unique commits from both branches and applies them one by one
- `git log` - view git history

## The anatomy of a Git commit

SHA1 hash:

- Each asset has it's own unique SHA-1 hash
- Example: f4f78b319c308600eab015a5d6529add21660dc1
- 40 characters long
- Take meta-info as the input (including commit message, committer, commit date, and tree hash) and produces a SHA-1 hash

## Practical Git commands

View the state of your branch:

```
git status
```

Quick view of commit history:

```
git log --oneline
```

View a specific commit:

```
git show 790dd94
```

Create (and checkout) a new branch:

```
git checkout -b US12345_my_cool_feature
```

Which branch do I have checked out?:

```
git branch
```

How do I switch branches?:

```
git checkout branch_name
```

Delete a branch:

```
git branch -d my_terrible_branch
```

I screwed everything up! Get me outta here:

(WARNING: this can result in unrecoverable data loss!)

```
git reset --hard
```

Checkout out a specific commit (you need to know the hash):

(WARNING: you need to either create a branch from this point, or checkout back to a branch before attempting to make commits, this mode is only for _viewing_ the checked out commit)

```
git checkout 790dd94
```

Stash your changes:

```
git stash
```

Recover (and _delete_ the stash) your latest stashed changes:

```
git stash pop
```

Recover (and _keep_ the stash) your latest stashed changes:

```
git stash apply
```

See all differences:

```
git diff
```

See differences of one file:

```
git diff -- /path/to/myfile.js
```

See differences of one file compared to another branch/hash (remove file to see full delta):

```
git diff <ref> -- /path/to/myfile.js
```


Rebase current branch _onto_ master:

(This stores any commits on the current branch that are not in master in memory, then fast-forwards your branch to master, then replays the stored commits on top)

```
git rebase master
```

Interactive rebase from a given commit (couple of options listed below):

```
git rebase -i master
git rebase -i 790dd94
```

## Resources

Learn Git Branching (by doing): https://learngitbranching.js.org

Git Visualization: https://git-school.github.io/visualizing-git

Great tutorials: https://www.atlassian.com/git/tutorials

The anatomy of a Git commit: https://blog.thoughtram.io/git/2014/11/18/the-anatomy-of-a-git-commit.html

Pluralsight course on rewriting Git history: https://app.pluralsight.com/library/courses/rewriting-git-history

Pre-commit javascript module: https://www.npmjs.com/package/pre-commit

Git hooks: https://githooks.com
