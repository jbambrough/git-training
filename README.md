# git-training

Sandbox repository for Git Training

## What is this?

This repository is a sandbox project for learning and improving Git techniques

## Setup

Have Git installed on your local machine

## Terminology

- `local` - your laptop
- `remote` - server where the repository is stored
- `tracked / untracked` - dfdf
- `stage` - dfdf
- `modified` - dfdf
- `branch` - dfdf
- `HEAD` - dfdf
- `SHA1 hash` - example: f4f78b319c308600eab015a5d6529add21660dc1. Unique identifier. Takes some input, produces a consistent output
- `Pull Request (PR)` - dfdf
- `Merge Conflict` - dfdf
- `rebase` - replays a set of commits on top of a specific base commit
- `interactive rebase` - a rebase that allows you to control how the changes are replayed

## Common Commands

- `git clone` - dfdf
- `git fetch` - sdfasdf
- `git pull` - fetch plus merge
- `git push` - dfdf
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
- Take meta-info as the input (including commit message, committer, commit date, and tree hash) and produces a SHA1 hash

## Practical Git commands

View the state of your code:

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

Create a new branch:

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

```
git reset --hard
```

Checkout out a specific commit (you need to know the hash):

```
git checkout 790dd94
```

See all differences:

```
git diff .
```

See differences of one file:

```
git diff /path/to/myfile.js
```

Rebase master branch onto my working branch (from your working branch):

```
git rebase master
```

Interactive rebase from a given commit (couple of options listed below):

```
git rebase -i master
git rebase -i 790dd94
```

## Resources

Git Visualization: `https://git-school.github.io/visualizing-git`

Great tutorials: `https://www.atlassian.com/git/tutorials`

The anatomy of a Git commit: `https://blog.thoughtram.io/git/2014/11/18/the-anatomy-of-a-git-commit.html`

Pluralsight course on rewriting Git history: `https://app.pluralsight.com/library/courses/rewriting-git-history`

Pre-commit javascript module: `https://www.npmjs.com/package/pre-commit`