# GitHub Tutorial

_by Amanda Lum_

---
## Git vs. GitHub

### What is Git?

Git is a system which keeps track of changes to code as different versions, which becomes the history that you can go back to or view. It runs in the command line, and displays all of the directories (called folders) that hold your files.

### What is Github?

Github is a website that allows you to keep your code in the cloud. It lets people collaborate with each other, since you can publish your repositories (or make them private!) for others to work on and add to. You can see the changes you have made.

### How are they different?
The difference between Git and Github is that Github needs to use Git, but Git can run on its own, **offline**. Github can track your changes more visually than Git does, and is more _convenient_ to use to work with others.

---
## Initial Setup

### How to make a Github account:

This step is fairly intuitive: Go to [the website.](https://github.com/)

How to set up your IDE:
[Just check this website for assistance!](https://github.com/hstatsep/ide50)

By this point you have come into contact with the *SSH key*. But what is this?

It's like a pair of keys, which let you work on projects related to Github without the effort of inputting your username and password. One is public which Github can use, the other one is  _exclusively_ for your computer to use. If the one you have matches with the one public key, upon using, you can log in on a website. 

---

## Repository Setup

* Do `mkdir first-repo`, which creates your directory.
* Type `cd first-repo`, allowing you to move into that directory.
* Once you have a directory, it's time to initialize it. When you initialize a directory `git init`, it means you have chosen to do your project in this directory. You thus turn it into a repository. You *must* do this step first, otherwise you cannot use the other Git commands!
* Make a file. You do this with `touch [name]`, for example `touch file.txt`. 
* Open the file with `c9 file.txt`, and add some text into it.
* Then do `git add .` and `git commit -m "[message]"`. Put a message so you can look at it and understand the changes you made to your file later on!

1. Create a new repository on Github and use the same name from your repository in your cs50 ide to this one.
2. Then, you need to make this new repository your remote, essentially linking the two so changes in your cs50 ide can be moved onto the remote. You can do this by using `git remote add origin [url]`, which creates the link. 
3. After that, once you make any changes do `git push -u origin master`. This pushes the changes to the remote now. From now on, you can do git push, which will do the same and will be _easier_ to type!

---
## Workflow & Commands
`Git status` is an essential command that you should be using often. Basically, use this command in between the process of adding, committing and pushing a file, and it will tell you if your files are to be added, committed, and if they are already pushed, and no changes have been made since your last push.

You do `git add` in order to signify that you want to save these changes. This adds it to the stage, so it's ready for saving. You then do `git commit -m ""`, which will save those changes. The `-m` is the precursor for the message you type in `""`, which is _very_ important. Write a commit message; its kind of like a comment on your code so you can go back to the commits and see what changes you made in the past. `Git push` means that you are officially publishing those changes to your Github remote. Your local changes are transferred to the remote, where others can easily interact with them.

---
## Rolling Back Changes
There are a few commands that can help you remove changes you have made to your code, just in case you make a mistake. These include `git checkout --file, git reset HEAD file, git revert HEAD.`

`Git checkout --file` means that you are undoing any changes that were made in your working directory. If you were working with another person, and edited a file that you didn't mean to, you can avoid merge conflicts by using the command. There, everything is back to normal now!

`Git reset HEAD file` means that you are taking a file out of the stage. This can be used if you accidentally add all of the files, when you mean to add a specific one only.

`Git revert HEAD` helps you go back to a prior commit. Use this command if you want to restart from a certain point.

---
## Error Handling
If you `git init` in the tilde for example, or the wrong directory, you can _easily_ fix this, don't worry. Do `rm -rf .git`, and it will uninitialize git.

If you want to completely remove a repository (local & remote), you can use the same command. Just specify the repository name, for example you have a repository called false-repo. Do `rm -rf false-repo`, and it will be promptly deleted. 

If you type `cd ~` by accident, you will be unable to cd into any of your repositories. To mend this, just do `cd ~` and you will be back to normal, and free to cd anywhere.

## Collaboration
If you would like to work with someone on the same repository, you can do this with forking and cloning. 

Forking works by 