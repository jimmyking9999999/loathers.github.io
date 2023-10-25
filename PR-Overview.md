# Submitting a Pull Request: a Simple Overview

## What is a Pull Request?

Let's say you've been on the ASS Discord for a while, or you've been messaging with various LASS contributors asking them to make changes to a script. You've submitted a few code snippets, and shared your ideas and concepts. They finally say: "OK, I think this is a great change -- can you put in a pull request on the project?"

Before we get into the protocol for a pull request, it's important to understand what exactly a pull request is. GitHub is a wonderful tool, and the best-in-class collaboration engine for coders and scripters throughout the world of programming. But it also can be quite opaque; if you aren't immersed in the specifics of Git workflow, it can be extremely hard to understand exactly what certain terms mean. At a high level, a **pull request** involves writing changes to code within a codebase on GitHub, letting the owners of that codebase know that you're suggesting changes, and giving them the opportunity to look through your changes and accept or reject them. It is, in essence, a request for the owners of the codebase to "pull" your changes in from your sample code into the base repository.

Writing a pull request, even for a simple task, can be a bit daunting -- but it doesn't have to be. This guide represents our best efforts to demystify that process and outline exactly how you would go about structuring a pull request for any LASS repository you'd like to see changes to. We'll be referring to pull requests as "PRs" for most of this guide, because we respect you, your time, and acronyms. One important caveat -- while this is a genericized guide, some projects may have additional hurdles that your PRs need to pass before being added to the base project. The most important example of this is [autoscend](https://github.com/Loathing-Associates-Scripting-Society/autoscend/blob/master/docs/CONTRIBUTING.md), which has a strict series of rules that must be followed to the letter if you want to add code to it. This guide is largely focused on contributing to TypeScript projects, as there are several layers in here (specifically all the Yarn stuff) that are non-obvious to a new contributor and save you a lot of heartache later.

## Basic Pull Requests (using the VSCode Terminal)

There are many, many ways to perform pull requests. There are three primary methods we want to highlight:

- Using GitHub Desktop
- Using the VSCode GUI
- Using VSCode & the VSCode Terminal

For this guide, we are going to focus on that last method, where we utilize the VSCode Terminal. There's nothing wrong with the other two methods, to be clear! We are only focusing on this method because we've found it to be the most straightforward to consistently walk through, as the terminal commands are not going to change over time, but the graphical user interface on GitHub Desktop and VSCode change with some frequency. Before we move on:

- If you are not comfortable with using the command line, try installing [GitHub Desktop](https://desktop.github.com/) and follow the [steps in this pull request guide straight from GitHub](https://docs.github.com/en/desktop/contributing-and-collaborating-using-github-desktop/working-with-your-remote-repository-on-github-or-github-enterprise/creating-an-issue-or-pull-request).
- If you need a bit of an outline on basic terminal usage, and want a Git installation walkthrough, [click here](#commandPrompt). Otherwise, read on!

When contributing to a project, there are 7 core steps to keep in mind.

**STEP 1: FORK THE PROJECT**

In non-programmer speak, a "fork" is simply a copy of a project; it is your copy that you can mess with code on without messing up the main project. To "fork" a GitHub codebase, go to the core project on the project's GitHub repository, and use the button in the top right corner. It looks like this!

![image](https://user-images.githubusercontent.com/8014761/149850326-b00d5268-12e7-4b74-ae9d-4d738ef1edf4.png)

**STEP 2: CLONE YOUR FORK ONTO YOUR LOCAL MACHINE**

Just making your fork is simply not enough. You must also "clone" the fork. I've always felt "cloning" is a weird term for it, but when we say "clone", we simply mean that you are downloading the code to your local machine and initializing all the fun Git architecture around it that allows you to modify and mess with your repository locally. To do this, you will get the URL of your forked project, like so:

![image](https://user-images.githubusercontent.com/8014761/149842243-09ad81ea-ab94-43cb-8475-6bc1375da62f.png)

Click the double-rectangles, next to the URL. After doing this, and after [navigating within the terminal](#navigateTerminal) to a folder you want to place your repository into, you will type the following into your command prompt, once you've navigated to a folder you'd feel comfortable working in:

```
git clone [the URL you copied]
```

**STEP 3: INSTALL DEPENDENCIES, IF IT'S A TYPESCRIPT PROJECT**

This is a pretty important step. Many LASS repositories are written in TypeScript. When you are working on a TypeScript project, there's a variety of tools and necessary repositories that your code editor (likely VSCode) will need to access in order to tell you if you've written your code correctly or properly format your final saves. Luckily, this is actually a very simple step. Just run the following code, which will force yarn to grab the project's dependencies and install them all into your project folder:

```
yarn install
```

**STEP 4: MAKE A BRANCH**

Branching is an important part of the PR process; it ensures that your copied repository stays relatively clean, and that your changes are confined to an easily accessed place that can be compared against the core development code. The best way to think about a branch is that it's just a segregated project folder that has some changes from the main folder. To make a branch, you will need to run the following commands. The first command shows you the branches, the second command adds a branch, and the third command switches you to your newly created branch.

```
git branch
git branch newBranchName
git switch newBranchName
```

One small syntax thing -- branch names cannot have spaces in them. So, "my-cool-branch" and "myCoolBranch" both work. But "my cool branch" does not.

**STEP 5: MAKE YOUR CODE CHANGES**

I can't walk you through this step. Just do whatever you want to do to the code. Fly freely, modifying code as you see fit to fulfill your basest desires. (Or just make the change you need to make, that works too.)

**STEP 6: COMMIT YOUR CHANGES TO YOUR BRANCH**

Now that you've made your changes (and saved them! YOU HAVE TO SAVE THEM!), you need to add your changes to the internet. To do this, you need to do a series of three commands, listed here. The first command adds your new files and ensures that Git understands that you've made changes. The second command applies a commit message, so that you know what your changes mean later on. And the final command pushes your branch up into the branch stored on GitHub.com, which will allow you to make the pull request we have been teasing this entire article. The "set-upstream" part is important because GitHub needs to know what your new branch is based on. Since you just forked the project, it is (obviously) based on origin.

```
git add .
git commit -m 'insert a message that describes what changes you've made to the code here'
git push --set-upstream origin nameOfBranch
```

**STEP 7: MAKE THE DANG PULL REQUEST**

Hey, guess what! You can finally make a pull request. To make the pull request, go to the upstream project (the one that you initially forked from) on GitHub, and click on the "New Pull Request" button.

![image](https://user-images.githubusercontent.com/8014761/149842328-f97ee8de-9859-45b3-aa0f-ed31ac615ce0.png)

From here, click on "compare across forks", like so.

![image](https://user-images.githubusercontent.com/8014761/149842360-8bf116ef-bf0d-4d5a-a792-e49b4725510d.png)

This will allow you to select your fork, and from your fork, select the branch you just made. You will be keeping "main" on the left and your fork/branch on the right, like so:

![image](https://user-images.githubusercontent.com/8014761/151403876-7e31e14e-e00c-461e-8672-d0277c970d74.png)

Type up a descriptive message about your PR, post it up, and wait for the project owner to see it and provide commentary on your beautiful changes. The world is now your oyster. You have made a PR!

## More Pull Request Resources

- [MakeAPullRequest.com](https://makeapullrequest.com/) features a video tutorial on how to make PRs that don't make project owners tear their hair out. It's a useful thing to watch, but may be a bit overwhelming to first time PR hopefuls.
- [This GIST](https://gist.github.com/Chaser324/ce0505fbed06b947d962) features a ton of commands that help outline ways to manage your own forks and clones and all that nonsense. It's a useful reference tool when you simply cannot remember what terminal command you need.
- If you are using VSCode for your development environment, there are ways to perform this whole process through VSCode's graphical user interface!
  - You'll want to use the "source control" tab, which you can activate by pressing CTRL + SHIFT + G. That's right, G is for GitHub!
  - Visit [this VSCode documentation page](https://code.visualstudio.com/docs/editor/github) for a walkthrough on how you'd go about using the tab and other extensions to create a fully GUI-powered pull request.

## Working in the VSCode Command Prompt <a name="commandPrompt"></a>

To open the terminal in VSCode, start by [installing and opening VSCode.](https://code.visualstudio.com/download) You will open the terminal by typing " CTRL + SHIFT + ` " or using the following menu in the VSCode top menu.

![image](https://user-images.githubusercontent.com/8014761/150451917-26357b70-e5e8-419d-b549-9a73b8ff1270.png)

From there, you'll see the following window on the bottom of the screen.

![image](https://user-images.githubusercontent.com/8014761/150452450-8279bc9d-22de-4ec9-96de-396314635fb5.png)

I am currently on Windows, so it shows Windows Powershell; if you're on a Mac or Linux machine, you will likely have something a bit different. It can be a bit intimidating to work in the terminal -- luckily, this how-to will show you essentially everything you need to do to utilize the terminal for pull requests.

<a name="navigateTerminal"></a>When you are in the terminal, there are two main commands you'll need to use -- `ls` ("list directory") and `cd` ("change directory"). When you use `ls`, it will list out the contents of the folder you're in:

![image](https://user-images.githubusercontent.com/8014761/150453426-7273150a-1d5f-491b-96c7-b76654839e3d.png)

Once you see the contents, you'll simply use `cd` to move into the folders you need to go to. While writing a `cd` command, you can use your tab key on your keyboard to autocomplete. (If you want to move up a directory, use `cd ..` -- that will move you up one folder.) I would recommend making a GitHub folder within your documents folder that can serve as a landing spot for any project you intend to create a pull request for.

As a last step, you should [go install Git](https://github.com/git-guides/install-git). That guide should walk you through the right install procedure for your local machine. Once you've done that, you're ready to start figuring out basic pull requests!
