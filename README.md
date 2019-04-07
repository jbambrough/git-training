# git-training

Sandbox repository for Git Training

## What is this?

This repository is a sandbox project for learning and improving Git techniques

## Setup

Have Git installed on your local machine

## Resources

Git Visualization: `https://git-school.github.io/visualizing-git`

Great tutorials: `https://www.atlassian.com/git/tutorials`

The anatomy of a Git commit: `https://blog.thoughtram.io/git/2014/11/18/the-anatomy-of-a-git-commit.html`

Pluralsight course on rewriting Git history: `https://app.pluralsight.com/library/courses/rewriting-git-history`

## Terminology

- `local` - dfdf
- `remote` - dfdf
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
- `git pull` - dfd
- `git fetch` - sdfasdf
- `git push` - dfdf
- `git reset` - dfdf
- `git diff` - dfdf
- `git stash` - dfdf
- `git merge` - dfdf
- `git rebase` - dfdf

## The anatomy of a Git commit

SHA1 hash:

- Each asset has it's own unique SHA1 hash
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

Create a new branch:

```
git checkout -b US12345_my_cool_feature
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

Rebase master branch onto my working branch:

```
git rebase master
```

Interactive rebase from a given commit (couple of options listed below):

```
git rebase -i master
git rebase -i 790dd94
```
