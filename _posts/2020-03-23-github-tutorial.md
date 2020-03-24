---
layout: post
title: About This Blog
tags:
- blog
- learning
- tech
---
# GitHub Basics Tutorial


### Introduction
I created this tutorial when I was a TA for the data structures class at Mills. Many of the students in that class had never used GitHub or any other version control tools before. The goal was to give them practice going through the motions of cloning, committing and pushing code. Although I personally use the command line tool in IntelliJ, many of the students haven't use the command line before and I wanted to limit the number of new ideas that I exposed them to, which is why this tutorial only uses GUIs.


This tutorial is intended to give you some hands-on practice forking, cloning, pulling and pushing using GitHub and an IDE (Eclipse or IntelliJ). Everything you do in this tutorial can also be achieved using the command line. This tutorial contains 7 steps, plus some additional resources. Some steps don’t use an IDE and therefore have the same steps regardless of IDE.


### 1. Create an Account
Go to https://github.com/join?source=header-home and fill out your information to create an account. You can create your account with your Mills email or a personal one; you can always add an additional email address to the account.

### 2. Fork the Repository
Forking the repository means that you now have your own copy of the entire code base in your GitHub account. It will not automatically update as the master changes. Your fork is your remote copy.
Go to the repository (https://github.com/[redacted]) and fork it (click the button at the top next to ‘Watch’ and ‘Star’).


### 3. Clone the Repository
Cloning the repository means you are getting a local version of your fork. The local version lives on your computer (or the computer you’re currently using) and is where you’ll make your changes. 
Open your preferred Java IDE (Eclipse or IntelliJ) and follow the instructions below.


**Eclipse**


To add the Git Repository view to Eclipse, click Window → Show View → Other… → Git → Git Repositories
Also add the Git Staging view from the same menu

Click “Clone a Git repository”
Navigate to your fork in GitHub, click “Clone or download” and copy the URL under “Clone with HTTPS”. If SSH is selected by default, click “Use HTTPS” then copy the URL.

Paste the URL into the URI line of the Source Git Repository dialog.
Leave protocol as https and provide your GitHub login credentials.

Click “Next”, select all branches (this is the default setting). Click “Next” again, then click “Finish”. Although we’re leaving all the settings at their defaults, take a moment to read through all your options, you might want to use them someday.


**IntelliJ**


From the landing page, select “Check out from Version Control” → Git

Navigate to your fork in GitHub, click “Clone or download” and copy the URL under “Clone with HTTPS”. If SSH is selected by default, click “Use HTTPS” then copy the URL.

Paste the URL into the Clone Repository dialog, click the test button to ensure the connection, then click clone. By default, IntelliJ will create a new folder for the repository with the same name.
Select “Create from Existing Sources”, then leave the rest of the settings at their defaults.
You may be required to provide your login credentials for GitHub to complete this process.

### 4. Make an Edit
For the purposes of this tutorial, we’re not using actual code. The only change you need to make is to add your name to the file AddYourNameHere.md and save it.
Usually, this is when you’ll write code.

### 5. Add Files + Commit Your Changes
Adding Files to staging means you’re moving them one step closer to your remote repository. Commiting files is putting a stopping point in your work. One way to think about this is like a checkpoint in a video game. You just completed something and you want to put a breakpoint into your work. 
For every commit you make, you need to add a description or ‘commit message’. For the change you made above, a description such as “Added my name to class list” is great. You don’t need to add the date or time or your name to this commit message; Git will do that for you.


**Eclipse**


First, open the Git Staging view and select the repository form the menu above by clicking the small yellow cylinder.
In Eclipse, saving a file will automatically add to the “Unstaged Changes” section of the Git Staging view. To add a file to staging, just drag it from “Unstaged Changes” to “Staged Changes” or click the green plus sign in the corned of “Unstaged Changes”.
In the “Commit Message” area, type your commit message, then click Commit. Notice that the file disappears from “Staged Changes”. This is because the file is Commited and ready to Push.


**IntelliJ**


At the top bar, click “VCS” → Commit. In the “Commit Message” area, type your commit message, then click Commit. Spend a moment to read all the options on the right sidebar, as you might want to use them sometime. Also see the diff view below, which shows you what changes you’re committing.


### 6. Push to Remote
Committing files adds a breakpoint to your work, but it’s not actually backed up remotely until you push your code. Usually, you’ll push code after achieving some expected outcome. You can (and often do) include multiple commits per push, but in this case we’re just going to push the one commit we made above.


**Eclipse**


Go to the “Git Repository” view, and right click the repository name. Click “Push Branch ‘master’...” → Enter your login credentials (if you’re having trouble with this, see troubleshooting below) → Preview → Push
    

**IntelliJ**


In the top menu bar, click VCS → Git → Push


Note that you see your commit message in the dialog. If you have multiple commits to push, you’ll see all of them listed. Click “Push”.

### 7. Open Pull Request
To see your pushed changes, go to your fork in GitHub. The URL will follow the format github.com/[[YOURUSERNAME]]/[redacted].

Click “New Pull Request” → “Create pull request”

You can now see your open pull request under Pull Requests in the upstream, which in this case is at [redacted].

### Additional Helpful Tutorials
[How to Import a GitHub Project Into Eclipse](https://github.com/collab-uniba/socialcde4eclipse/wiki/How-to-import-a-GitHub-project-into-Eclipse)


["Learn Git Concepts, Not Commands"](https://dev.to/unseenwizzard/learn-git-concepts-not-commands-4gjc)


[Adding a Local Project to GitHub in IntelliJ - Video](https://www.youtube.com/watch?v=mf2-MOl0VXY)


[What Is a .gitignore File?](https://git-scm.com/docs/gitignore)


[Git and GitHub for Beginners](https://product.hubspot.com/blog/git-and-github-tutorial-for-beginners)

### Troubleshooting
If you’re trying to push your code and keep getting prompted for your login credentials, it’s possible that your two factor authentication is causing the problem. To continue, either temporarily disable two factor authentication or clone using SSH.

### Glossary
+ **Branch**: a version of the codebase that you want to keep separate from the main branch
+**Commit**: to save a checkpoint in your code (this does NOT push the code to remote, so it’s not backed up after you commit)
+**Diff**: the differences between two files
+**Fork**: create a new version of a project for yourself
+**.gitignore**: a file in your repository which tells git which files to leave untracked
+**Local**: files and code that you have on the computer that you’re working on
+**Merge**: to combine two branches into one
+**Merge conflict**: two files that you’re trying to merge have incompatibilities that you need to handle. You need to either choose one of the files or manually combine them into a single file.
+**Pull**: to bring code from the remote repository to your local machine
+**Push**: to bring code from your local machine to the remote repository
+**Remote**: files and code that are saved in GitHub, but not on the computer that you’re using
+**Repository**: a collection of files stored on GitHub, sort of a folder
+**Upstream**: a remote repository that is common to all people working on the project. This is where you fork from.
