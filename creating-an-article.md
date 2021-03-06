# Creating an Online Article

## Introduction

I have been wanting to write an article about git for a few months now. After several hours of research I am satisfied with the content I will be able to create, but I want to document my process so that through my learning and research you might be able to learn as well. I created two articles out of my research. The first, [Understanding Git](./understanding-git.md), provides a base level understanding of what git is, and the subsequent article, [Git Survival Guide](./git-survival-guide.md), explores various git commands that are used to be effective in a workplace environment.

## Literature Review

There is a wealth of information for the git utility. Web developers, software architects, code enthusiasts, and a multitude of other disciplines use git constantly throughout the day. The uses for git are endless: version control, keeping code bases backed up, enabling thousands of people to work on the same project seamlessly, and allowing the rest of the internet to view your code. As with any extremely popular technology, there are a vast amount of opinions on how to most effectively use git, and many of them are directly opposed to each other. This, among other things, can make git a very hard technology to learn. There are several resources that teach git at an intermediate or high level, but I have found few that explain it to me as if I had no idea what was going on.

My aim is to provide a git guide that provides a deep and intuitive understanding of what the different commands in git are so that a newcomer does not need to be in the dark about what they are doing. Through research I will be able to adequately explain the different “essential” commands and provide simple introductions to the other commands that are more hotly debated. Finally, I hope my article will be a place for newcomers and seasoned programmers alike to reference when they need to remember the correct syntax for a git command.
Another important part of my research is in effective instructional writing. I intend for this guide to be published online on Medium, and I would love to be able to help multiple new developers understand what some of the most important commands in git are, on a deeper level than just memorization. When I started using git, I was just told to use the commands, “git add, git commit, and git push.” That is all I was given. I had no idea it was such a powerful utility.

## Understanding Technical Writing

The research about technical writing frequently mentions the effectiveness of using images. The posts discuss the importance of using images to draw the user into the article through visual interest, but also as a way of explaining. Patel says, “all of us our visual learners… our brains are wired that way.” Many of the articles I read did use visual to try to explain these different commands, but they always have confusing branches and letters and numbers in different places. I tried multiple times when I started out to understand what these visuals were trying to teach, but I just could not. I hope to provide more intuitive visuals to help my audience understand git. In the following paragraphs I will provide two examples from research of how I intend to do this.
An Atlassian article on saving changes states that, “The primary function of the git add command, is to promote pending changes in the working directory, to the git staging area.” Using these visual words, I will create an image of 3 steps: a working directory, a staging area, and a remote repository.

In Ryan Abel’s article, he discusses the importance of deleting branches locally and remotely. My current work is currently going through the process of doing just this because our repository has gotten completely out of control. I will get permission to take pictures of what our current repository branch structure looks like and discuss how difficult it is to understand which branches are important and which are not. I will then show what a clean git repository should look like and show a picture of what that would look like. I believe this would be a powerful visual image to people to help get them on board with deleting branches. I would also discuss how it is possible to archive branches with a tag, just in case people are afraid of deleting data they need. Abel’s blog does not discuss this option.

## Analyzing What Needs To Be Talked About

I went into this thinking that I was mostly going to be using my own knowledge to create a git survival guide. My research has proven me very wrong. The examples on several websites are much better than I could have come up with on my own. I do believe, however, that I am going to be able to meet a need that has not been met yet: consolidating all the helpful information into one place. I want to make sure my post is well organized so that people can easily find information, and I want it to be complete enough, so people do not need to go to other sites to use these commands. I do, however, want to provide a multitude of additional resources so people can educate themselves on how these commands work, because that is not the emphasis of my article.

It is important, however, to consider how I came to the decisions about what information to include. Both the gitflow Workflow article and Abel’s article discuss deleting branches. I have also found in my own personal work that deleting get branches makes it easier to keep track of what is happening. Some people still do not do this though, so it will be an important point to bring up.
Time is money, and so another tip I will be including is from Kurt Dowswell. He teaches about using git Bash Aliases to reduce the amount of letters we need to type to make these git commands happen. In a workday, I will typically type around 200 git commands, so even small changes make a big difference in a workday. I have implemented Dowswell’s tips into my workflow, and am very satisfied with the results. I believe people should always try and find shorter and faster ways to do the same thing, and that is why I will discuss git Bash Aliases.

Git reflog is a command that basically shows you a history of everything that you have done. It is almost like Microsoft Word’s undo explorer. Sometimes when you are working on a git branch things will just start to turn really south and you need to go back to where you were before everything was messed up. git reflog shows you exactly what happened so you can reset your current status to where you need to be. I am including the command because it has saved me several times from being totally lost, and my other develop friends vouch for it as well.

Git rebase -i is a command that helps to maintain a clean git history. This command is a little bit more controversial in the git community. Abel’s article discusses the importance of the command, stating, “A few common commits on my branches are: ‘WIP,’ ‘Run Rubocop,’ and ‘Fix typo.’ There is no reason these commits should be remembered in the history books of a project.” git rebase -i makes it so those messages can be removed or combined together to better keep track of what changes were made in a sensible way. I have been using this command and it has helped me in some situation. However, after just reading the article again I have a better understanding of how to use the command to maintain an even clearer git history.

## Conclusion

Missing research includes data about how effective the different git workflows are. I believe this data in itself is not tangible but looking at what major companies do could give light to what is actually effective. An interesting research project could be what similarities and differences are there in the git workflows of the top 1000 companies using git. There is not a beginner friendly resource for getting started with git and getting integrated into an office workflow, and I believe my article will help to fill that need. You can read my article [here](./understanding-git.md).

## Works Cited

Patel, Neil. “8 Data-Driven Tips for Using Images in Blog Posts.” HubSpot, Hubspot Inc, 31 Oct. 2014, [https://blog.hubspot.com/marketing/images-in-blog-posts-tips](https://blog.hubspot.com/marketing/images-in-blog-posts-tips)

“Saving Changes.” Atlassian, Atlassian, [https://www.atlassian.com/git/tutorials/saving-changes](https://www.atlassian.com/git/tutorials/saving-changes)

Abel, Ryan. “Four Steps To Maintaining a Clean Git History.” Atomic Object, B Corp, 23 Apr. 2017, [https://spin.atomicobject.com/2017/04/23/maintain-clean-git-history/](https://spin.atomicobject.com/2017/04/23/maintain-clean-git-history/).

“Gitflow Worfklow.” Atlassian, Atlassian, [https://www.atlassian.com/git/tutorials/comparing-workflows/gitflow-workflow](https://www.atlassian.com/git/tutorials/comparing-workflows/gitflow-workflow)

Dowswell, Kurt. “Git Bash Aliases.” Kurt Dowswell, 07 Sep. 2017, [http://kurtdowswell.com/software-development/git-bash-aliases/](http://kurtdowswell.com/software-development/git-bash-aliases/)
