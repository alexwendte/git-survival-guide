# Understanding Git

## Introduction

Git is the backbone to most hobby and enterprise-grade projects. Git is a version control system which enables users to easily and efficiently back up code, keep track of changes to a codebase, and collaborate with other developers. It can be very confusing to learn because of the lack of beginner-friendly resources online that are filled with `git jargon`. In this article I hope to establish a base-level understanding of what git is and how it works. I will do this through applying an analogy comparing writing and saving a text article to writing code and "saving" it through git. If you already feel comfortable using git, feel free to read my [Git Survival Guide](./git-survival-guide.md) that can provide you with tools to improve your git workflow.

## The Analogy

### Commit, Add, and Log, and Diff

Imagine that you start typing and make great progress on writing an article. Afterwards, you will certainly want to save the document so that if Windows decides to mysteriously shut down you won't have to redo all the progress you made. How do you save the file? For the sake of our example, let us say that you want to keep a record of all the previous times you have saved the article. In that case, you would go to file → save as → and then give the article a meaningful title to help you know how this particular save contributed to the article. By giving the documents different names, you will have the ability to go back to previous edits later. For example, if you realize a few saves down the road that you liked your old introduction better, you can just copy it from an earlier save and paste it into the new one.

Git has the same functionality, it just works a little differently. After writing enough code, you will probably want to “save” your progress. With git, you can save your changes and provide a helpful message denoting which changes you made. The way you save your changes (or in git language `commit` your changes) is through [git add](./git-survival-guide.md/#git-add) and [git commit](./git-survival-guide.md/#git-commit), which are explained in the essential git commands section. You can view previous commits through [git log](./git-survival-guide.md/git-log) and you can view the changes that were made in the commits through [git diff](./git-survival-guide.md/#git-diff). Just like learning any other utility, it may take some time to become familiar with the process of git. I guarantee you that once you understand, you will be amazed at how powerful of a tool it is. Let's get back to the analogy to explore 2 more git features.

### Push, Clone, and Pull

After editing and saving the article several times, you decide you are done working for the day. After a productive day of writing you decide you want to keep your article safe throughout the night, in case your hard drive were to go out. But the big question is, how do you do that? You decide to upload your article to Google Drive to keep it safe in the cloud. If you ever need access to the article, from a different computer or if you accidentally delete it from yours you can simply download it from Google Drive.

Again, you can do the same thing with git. After a day of working on some code (or really whenever you want) you can take the commits (saves) that exist locally on your computer and you can push them up to a remote server that will store them for you. This can be accomplished through using [git push](./git-survival-guide.md/#git-push). You can also "download" the code to your computer by using [git pull](./git-survival-guide.md/#git-pull) or [git clone](./git-survival-guide.md/#git-clone) depending on what is on your local machine. This is where the popular [GitHub](https://github.com) comes into play. GitHub is like Google Drive in our example for our collection of git commits. Now we get to discuss one of the most exciting functionalities that git makes extremely easy: collaboration.

### Branch

Because the article is online, other people have access to it if you give it to them. Let's say you want your friend, Brianna, to take a look at your article and edit it. In order to do so, you would send her a link to your article and she would click on it and be able to access the article on Google Drive. Brianna would then download the article start editing it. Whenever she saves the file she will create a new save titled, "Article-Brianna-Edits" so that it is clear which version of the article it is. Now, whenever she uploads the completed edits to Google Drive, you would be able to see the new file "Article-Brianna-Edits" along with the original file you uploaded.

This is similar to branching in git. Whenever you have changes that you want to make on a codebase, it is good practice to create a [git branch](./git-survival-guide.md/#git-branch). On this branch, you should only make changes that are relevant to the goal you are trying to achieve. For example, you could have a git branch titled "update-npm-packages" or "fix-header-css-bugs." This way, it is very clear what changes you are making, and it leaves your original code-base intact, almost like using "Save As" in Microsoft Word.

### Merge

When you look at the changes Brianna made to your article, you will need to include some of them into your draft of the article, but some of them you might not want to include. The way you can tell there are differences is you will compare the article you uploaded on Google Drive with the article she uploaded on Google Drive and find the differences. When you are satisfied that you have the changes implemented that you like, you can save the changes on your document and safely delete "Article-Brianna-Edits" because it is not needed any longer.

There is a similar workflow with git. Using the command [git merge fix-header-css-bugs](./git-survival-guide.md/#git-merge) you are able to combine the changes from the fix-header-css-bugs branch and apply them to your current branch. If there were changes that were made in the fix-header-css-bugs branch and the current branch you are on, you are able to pick which change you would like to keep and throw the other one away.

## Next Steps

I hope the analogy of writing an article was helpful to your basic understanding of git. There are very clear differences, but I believe the basic concepts are similar. You can learn to employ git effectively by reading the [Git Survival Guide](./git-survival-guide.md/) which will equip you with the git commands necessary to succeed in the workplace. If you are interested in the process I took in creating this article you can read [Creating An Article](./creating-an-article.md)
