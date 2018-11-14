# The Git Survival Guide

## Introduction

## Table of Contents

- [The Git Survival Guide](#the-git-survival-guide)
	- [Introduction](#introduction)
	- [Table of Contents](#table-of-contents)
	- [Literature Review](#literature-review)
		- [Technical Writing](#technical-writing)
		- [What needs to be talked about](#what-needs-to-be-talked-about)
		- [Conclusion](#conclusion)
	- [Understanding Git](#understanding-git)
	- [Essential Git Commands](#essential-git-commands)
		- [Git Add](#git-add)
		- [Git Commit](#git-commit)
		- [Git Status](#git-status)
		- [Git Diff](#git-diff)
		- [Git Log](#git-log)
		- [Git Push](#git-push)
		- [Git Pull](#git-pull)
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

## Literature Review

There is a wealth of information for the Git utility. Web developers, software architects, code enthusiasts, and a multitude of other disciplines use Git constantly throughout the day. The uses for Git are endless: version control, keeping code bases backed up, enabling thousands of people to work on the same project seamlessly, and allowing the rest of the internet to view your code. As with any extremely popular technology, there are a vast amount of opinions on how to most effectively use Git, and many of them are directly opposed to each other. This, among other things, can make Git a very hard technology to learn. There are several resources that teach Git at an intermediate or high level, but I have found few that explain it to me as if I had no idea what was going on.

My aim is to provide a Git guide that provides a deep and intuitive understanding of what the different commands in Git are so that a newcomer does not need to be in the dark about what they are doing. Through research I will be able to adequately explain the different “essential” commands and provide simple introductions to the other commands that are more hotly debated. Finally, I hope my article will be a place for newcomers and seasoned programmers alike to reference when they need to remember the correct syntax for a Git command.
Another important part of my research is in effective instructional writing. I intend for this guide to be published online on Medium, and I would love to be able to help multiple new developers understand what some of the most important commands in git are, on a deeper level than just memorization. When I started using git, I was just told to use the commands, “git add, git commit, and git push.” That is all I was given. I had no idea it was such a powerful utility.

### Technical Writing

The research about technical writing frequently mentions the effectiveness of using images. The posts discuss the importance of using images to draw the user into the article through visual interest, but also as a way of explaining. Patel says, “all of us our visual learners… our brains are wired that way.” Many of the articles I read did use visual to try to explain these different commands, but they always have confusing branches and letters and numbers in different places. I tried multiple times when I started out to understand what these visuals were trying to teach, but I just could not. I hope to provide more intuitive visuals to help my audience understand git. In the following paragraphs I will provide two examples from research of how I intend to do this.
An Atlassian article on saving changes states that, “The primary function of the git add command, is to promote pending changes in the working directory, to the git staging area.” Using these visual words, I will create an image of 3 steps: a working directory, a staging area, and a remote repository.

In Ryan Abel’s article, he discusses the importance of deleting branches locally and remotely. My current work is currently going through the process of doing just this because our repository has gotten completely out of control. I will get permission to take pictures of what our current repository branch structure looks like and discuss how difficult it is to understand which branches are important and which are not. I will then show what a clean git repository should look like and show a picture of what that would look like. I believe this would be a powerful visual image to people to help get them on board with deleting branches. I would also discuss how it is possible to archive branches with a tag, just in case people are afraid of deleting data they need. Abel’s blog does not discuss this option.

### What needs to be talked about

I went into this thinking that I was mostly going to be using my own knowledge to create a Git survival guide. My research has proven me very wrong. The examples on several websites are much better than I could have come up with on my own. I do believe, however, that I am going to be able to meet a need that has not been met yet: consolidating all the helpful information into one place. I want to make sure my post is well organized so that people can easily find information, and I want it to be complete enough, so people do not need to go to other sites to use these commands. I do, however, want to provide a multitude of additional resources so people can educate themselves on how these commands work, because that is not the emphasis of my article.

It is important, however, to consider how I came to the decisions about what information to include. Both the Gitflow Workflow article and Abel’s article discuss deleting branches. I have also found in my own personal work that deleting get branches makes it easier to keep track of what is happening. Some people still do not do this though, so it will be an important point to bring up.
Time is money, and so another tip I will be including is from Kurt Dowswell. He teaches about using Git Bash Aliases to reduce the amount of letters we need to type to make these git commands happen. In a workday, I will typically type around 200 git commands, so even small changes make a big difference in a workday. I have implemented Dowswell’s tips into my workflow, and am very satisfied with the results. I believe people should always try and find shorter and faster ways to do the same thing, and that is why I will discuss Git Bash Aliases.

Git reflog is a command that basically shows you a history of everything that you have done. It is almost like Microsoft Word’s undo explorer. Sometimes when you are working on a git branch things will just start to turn really south and you need to go back to where you were before everything was messed up. Git reflog shows you exactly what happened so you can reset your current status to where you need to be. I am including the command because it has saved me several times from being totally lost, and my other develop friends vouch for it as well.

Git rebase -i is a command that helps to maintain a clean git history. This command is a little bit more controversial in the git community. Abel’s article discusses the importance of the command, stating, “A few common commits on my branches are: ‘WIP,’ ‘Run Rubocop,’ and ‘Fix typo.’ There is no reason these commits should be remembered in the history books of a project.” Git rebase -i makes it so those messages can be removed or combined together to better keep track of what changes were made in a sensible way. I have been using this command and it has helped me in some situation. However, after just reading the article again I have a better understanding of how to use the command to maintain an even clearer git history.

### Conclusion

Missing research includes data about how effective the different git workflows are. I believe this data in itself is not tangible but looking at what major companies do could give light to what is actually effective. An interesting research project could be what similarities and differences are there in the git workflows of the top 1000 companies using git. There is not a beginner friendly resource for getting started with Git and getting integrated into an office workflow, and I believe my article will fill that need.

## Understanding Git

Before jumping into explaining various git commands I want to make sure we have a base-level understanding of what git is and how it works on a conceptual scale. I have read multiple guides and tutorials on git and I have found many of them fail to explain git as if someone has never used it before. If you feel comfortable using git, you can skip to the [essential commands](#essential-git-commands).

Git is a version control system which enables users to easily and efficiently keep track of changes to a codebase, collaborate with other developers, and backup code. I will use an analogy to help explain git.

Think of a Microsoft Word document. Say you start typing and make some great progress on an article. After such great work you will certainly want to save it so that if Windows decides to mysteriously shut down you won't have to redo all the progress you made. How do you save the file? For the sake of our example, let us say that you want to keep a record of all the previous times you have saved the article. In that case, you would go to file -> save as -> and then give the article a meaningful title to help you know how this particular save contributed to the article. This way, if you realize a few saves down the road that you liked your old introduction better, you can just copy it from an earlier save and past it into the new one.

The same exact things happens with git. When you decide you have written enough code that you would like to mark your progress, you are able to "save" your changes and provide a helpful message denoting what changes you made. The way you save your changes (or in git language `commit` your changes) is through [git add](#git-add) and [git commit](#git-commit) which are explored in the essential git commands section. You can view previous commits through [git log](#git-log) and you can view the changes that were made in the commits through [git diff](#git-diff). Just like learning any other utility, it will take some time to be familiar with the process of git, but I guarantee you, once you understand, your mind will be blown with how powerful a tool it is and how much headache it can save you. Let's go back to the example to explore another few git features.

After several sessions of inspiration you decide you are done working for the day. After such a productive day, you decide you want to keep your article safe in case your hard goes out on you in the middle of the night. How do you do that? You decide to upload your article to DropBox to keep it safe in the cloud. This also has the added benefit that other people whom you give access to your article can download their own version of the article, and make changes to it. If you give them enough permission, they can even make changes to the article that is in DropBox. They cannot, however, change the article that is on your computer unless you download the article they uploaded and apply the changes yourself.

Again, you can do the same thing with git. After a day of working on some code (or really whenever you want) you can take the commits (saves) that exist locally on your computer and you can push them up to a remote server that will store them for you. Just like with DropBox, other people can access your code if you give them permission. This can be accomplished through using [git push](#git-push). This is where the popular [GitHub](https://github.com) comes into play. GitHub is like DropBox in our example for our collection of git commits.

I hope the analogy of a Word document was helpful to your basic understanding of git. There are very clear differences, but I believe the basic concepts are similar. Continue reading to learn some of the essential git commands, commands that are more advanced but powerful, and commands that are helpful on a day to day basis.

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

</p></details>

### Git Status

Usage

```
git status
// output ↓
-> On branch master
-> Your branch is up to date with 'origin/master'.
->
-> Changes to be committed:
->  (use "git reset HEAD <file>..." to unstage)
->
->        modified:   git-survival-guide.md
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
-> commit 1ee872ab45d5eb69fd668720d2435f8da38881b3 (HEAD -> master, origin/master)
-> Author: Alex <alex@wendtedesigns.com>
-> Date:   Tue Nov 13 20:51:57 2018 -0600
->
->     adds git diff
->
-> commit 2adc818d3c076bfaa5837d5fc03eefe19921bf52
-> Author: Alex <alex@wendtedesigns.com>
-> Date:   Tue Nov 13 20:40:04 2018 -0600
->
->     adds expand to each explanation section
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
