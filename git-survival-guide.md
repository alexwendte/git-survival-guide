# The Git Survival Guide

## Introduction

My journey with git has been similar to most people. I started out just using git to store my personal projects on a remote repository through `git add`, `git commit`, and `git push`. When I started my first web development job I was overwhelmed by their git workflow and the added complexity that came with it. I learned more about git in that first week then I learned in a whole year of building my own apps. I started to research the best way to maintain a clean git history and how to use git to its fullest potential. There are several commands I have found myself using very frequently that have made my git workflow much smoother. I figured I would share with git newcomers a collection of the commands I use every day in order to help facilitate their git productivity at work.I hope this will also be an excellent resource for git veterans when they forget syntax or want to explore different ways of accomplishing the same task.

If you are new to git I recommend reading my recent post [Understanding Git](./understanding-git.md) before reading the commands below as it will help give context for why we need to use the commands.

## Table of Contents

- [The Git Survival Guide](#the-git-survival-guide)
	- [Introduction](#introduction)
	- [Table of Contents](#table-of-contents)
	- [Essential Git Commands](#essential-git-commands)
		- [Git Add](#git-add)
		- [Git Commit](#git-commit)
		- [Git Status](#git-status)
		- [Git Diff](#git-diff)
		- [Git Log](#git-log)
		- [Git Push](#git-push)
		- [Git Pull](#git-pull)
		- [Git Clone](#git-clone)
		- [Git Checkout](#git-checkout)
		- [Git Reset](#git-reset)
		- [Git Merge](#git-merge)
		- [Git Branch](#git-branch)
		- [Git Reflog](#git-reflog)
	- [Advanced Git Commands](#advanced-git-commands)
		- [Git Rebase](#git-rebase)
		- [File Specific "Merge"](#file-specific-merge)
		- [Amend a Commit](#amend-a-commit)
		- [Tags](#tags)
	- [Utility Git Commands](#utility-git-commands)
		- [Comparing Commits (..)](#comparing-commits-)
		- [Diffing Branches](#diffing-branches)
		- [Checking Out A Commit](#checking-out-a-commit)
		- [Name Only Diff](#name-only-diff)
		- [Remove Cached Git Files](#remove-cached-git-files)
	- [Bonus Tips](#bonus-tips)
		- [Git Aliases](#git-aliases)
		- [Git Flow Workflow](#git-flow-workflow)
		- [Chaining Commands](#chaining-commands)
	- [References](#references)

## Essential Git Commands

### Git Add

Usage

```
// adds everything at and below current console directory
git add .
```

```
// adds a specific directory or path relative to current console directory
git add <path(s) to directory or file(s)>
```

<details><summary>Explanation</summary><p>

`git add` is used to elevate the changes you chose from your working directory (where you are adding code and deleting code) into the staging area. The staging area is where you put code before you are ready to actually save it by using git commit. When there are a lot of changes that are made it is handy to be able to look at the changes one file at a time and after you are satisfied with the file's changes, you you can add it to the staging area.

</p></details>

### Git Commit

Usage

```
// saves the changes in the staging area into a commit with a message
git commit -m "updates React to version 16.6.1"
```

<details><summary>Explanation</summary><p>
`git commit` is used to take the changes in the saving area and save them so that you can come back to the changes at a later time. This enables you to easily see the line-by-line differences between various commits and branches.

**NOTE** Commits are essential to a clean and easy to understand git repository. It is extremely important that you provide clear commit messages detailing the changes you made. If one of your coworkers looks at your commit messages they should be able to see how each commit affected the codebase. You don't need to go into specific code changes, they can look at the `git diff` for that, but the message should be a clear summary about the work you did.

</p></details>

### Git Status

Usage

```
git status
// output ↓
→ On branch master
→ Your branch is up to date with 'origin/master'.
→
→ Changes to be committed:
→  (use "git reset HEAD <file>..." to unstage)
→
→        modified:   git-survival-guide.md
```

<details><summary>Explanation</summary><p>

`git status` shows you the state of your current branch. It will show you changes that are in the working directory, changes that are in the staging area, files that were deleted, what branch you are on, your current relation to the upstream branch, and several other things.

</p></details>

### Git Diff

Usage

```
// shows the differences in the current working directory against HEAD (normally the last commit)
git diff
```

```
// show the differences in the specified files against HEAD
git diff <path(s) to directory or file(s)>
```

<details><summary>Explanation</summary><p>

`git diff` is one of the most helpful commands for ensuring the changes you made were intentional. The output of git diff can take some getting use to to understand. Basically git diff shows you is the difference between the lines that were changed. You will see "+" next to lines that were added relative to HEAD and "-" next to lines that were deleted relative to HEAD.

view [Diffing Branches](#diffing-branches) for viewing the differences between git branches.

</p></details>

### Git Log

Usage

```
git log
// output ↓
→ commit 1ee872ab45d5eb69fd668720d2435f8da38881b3 (HEAD → master, origin/master)
→ Author: Alex <alex@wendtedesigns.com>
→ Date:   Tue Nov 13 20:51:57 2018 -0600
→
→     adds git diff
→
→ commit 2adc818d3c076bfaa5837d5fc03eefe19921bf52
→ Author: Alex <alex@wendtedesigns.com>
→ Date:   Tue Nov 13 20:40:04 2018 -0600
→
→     adds expand to each explanation section
```

<details><summary>Explanation</summary><p>

`git log` shows you your commit history. **TIP** Make sure you press "q" to get out of `git log` and not "ctrl + c". "ctrl + c" will sometimes mess up your terminal.

Look at [Comparing Commits (..)](#comparing-commits-) for an even more useful feature of `git log`.

</p></details>

### Git Push

Usage

```
//

```

<details><summary>Explanation</summary><p>

</p></details>

### Git Pull

Usage

```
//

```

<details><summary>Explanation</summary><p>

</p></details>

### Git Clone

Usage

```
// clones the repository into your current directory
git clone <your-remote-repository>
```

<details><summary>Explanation</summary><p>

`git clone` is used to take a remote git repository, which can be online or simply in a different directory, and make it a local repository that you can interact with like any other repository. The remote repository remains unchanged.

</p></details>

### Git Checkout

Usage

```
//

```

<details><summary>Explanation</summary><p>

</p></details>

### Git Reset

Usage

```
//

```

<details><summary>Explanation</summary><p>

</p></details>

### Git Merge

Usage

```
//

```

<details><summary>Explanation</summary><p>

</p></details>

### Git Branch

Usage

```
//

```

<details><summary>Explanation</summary><p>

</p></details>

### Git Reflog

Usage

```
//

```

<details><summary>Explanation</summary><p>

</p></details>

## Advanced Git Commands

### Git Rebase

Usage

```
//

```

<details><summary>Explanation</summary><p>

view [yo](https://hi) for further reading.

</p></details>

### File Specific "Merge"

### Amend a Commit

### Tags

## Utility Git Commands

### Comparing Commits (..)

### Diffing Branches

### Checking Out A Commit

### Name Only Diff

### Remove Cached Git Files

## Bonus Tips

### Git Aliases

### Git Flow Workflow

### Chaining Commands

## References
