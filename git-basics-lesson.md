
#  Git Basics

---

# Learning Objective

- Understand what `git` is and where it is used
- Make your first, "commit"


---


# Getting Set Up

**Mac**

If you are a mac user, you have git through Xcode CLI tools. You can check if you have it by typing `git` from anywhere in your Terminal.

**Windows**

If you are a Windows user, download it if you don't already have it:
[http://git-scm.com/downloads](http://git-scm.com/downloads).

You can use Git Bash (included with Git) for all Terminal and git interactions. To launch, Start Menu -> Programs -> Git -> Git Bash.


---


# Where is git?

- Once you've installed git, you can verify it has been installed by opening up the Terminal and typing `git`

````bash
$ git
````

- If you see a 'command not recognized' error, you probably haven't installed git


---


# What is `git`?

- A **version control system** meant to make it easier to have multiple versions of code, sometimes across multiple developers or teams.

- At its most simple, `git` helps with the `indexv1.html, indexv2.html, indexv3FINAL.html` problem.

- At its most complex, git allows developers to work together worldwide on code without stepping on each other's toes


---


# Why learn `git`?

- Allows you to see the changes you make to your code and easily revert them

- By pushing your git repositories to GitHub, you'll have a developer portfolio automagically!

- You'll eventually push your code to a remote server using `git` - your application's **host**, so you can release your webpage or web application to the world


---


# Don't get confused - `git` vs GitHub.com

- **git** is a version control system that takes snapshots of your code at certain points in development

- These snapshots are stored in a 'repo', or 'repository' on your local machine

- **GitHub.com** is a website that hosts git repositories on a remote server

- We'll be able to troubleshoot your issues more easily if you're able to identify which of these two separate things you're having trouble with


---


# Configuring git

Your commits will have your name and email attached to them. Before we put anything up in public, let's make sure they're correct!

**Setting** your name and email:

```bash
$ git config --global user.name "Liza Ramo"
$ git config --global user.email "lizaiscOol@hotmail.com"
```

To see if it worked, you can **retrieve** these values:

```bash
$ git config --global user.name
> # Your name will display here: "Liza Ramo"

$ git config --global user.email
> # Your email will display here: "lizaiscOol@hotmail.com"
```


---


# Getting started

- Before using `git`, you'll need a **project** to use it with

- A **project** is any directory (folder) full of files

- Using the CLI, create a new directory, create a few files inside of it, and `cd` into the new directory.


---


# Getting started: `git init`

- Once you're in the top level of your project's directory, run the `git init` command to initialize git.

````bash
$ git init
````

- You only need to run this command **once** per project.

- Unsure if you've initialized yet? Try running `git status` - if you get a `fatal error`, you haven't run `git init` yet.


---


# Making your first commit

- A commit is a 'snapshot' of your project at a certain time

- It tracks all of the changes you've made since the last commit

- Two steps to make the commit:

  - **Stage** your files: choose which files to add to your repo.

  - **Commit** tell git to make your commit with an accompanying descriptive message.


---

# Staging, or Adding, files

To stage (add) all of your new files to your new git repo:

````bash
$ git add .
````


---


# Making a commit

Once your files are staged, you can make a commit using the `git commit` command.

The `-m` flag stands for "message". This is a few words describing what this commit is about. Devs typically make a few commits per day. The message will elaborate on what has changed since their last commit.


````bash
$ git commit -m "Initial commit."
````

---


# Tip: Use descriptive commit messages

If you use descriptive commit messages, it'll be much easier to see how your project has progressed later on.

````bash
# This is the customary message when staging files for the first time:
$ git commit -m "Initial commit."
````

````bash
$ git commit -m "Added 'about' to the navigation bar and a page for it."
````

````bash
$ git commit -m "Closes ticket #15 by adding a blue background on hover."
````

---


# Tip: If you forget a commit message...

If you forget to add a commit message and hit enter:

````bash
$ git commit [Enter]
````

You may end up in what's called **vim**. To exit this, simply hit the escape key, then type the following.


```bash
$ :q!
```

---

# `git status`

- You can always run this command 'for free', meaning with no repercussions.

- Will help you figure out if:

  - `git` is initialized for this project

  - what files are staged

  - what files have been changed since the last commit


---


# Tip: you need files!

- A common beginner mistake is to get excited about starting your new project and try to `git init` before you have any files

- git doesn't work unless you have files to track!


---


# Tip: use `git log`

- Curious what commits have been made so far?

- `git log` will show you what commits have been made so far

````bash
$ git log
commit 4038fb143edfc068264479cce855619730d6edca
Author: Zach Feldman <zach@nycda.com>
Date:   Tue Nov 25 17:05:28 2014 -0500

    Tracking stuff.

commit 74ee59894ef22fd714bf3ffb06f2ef4cf43be0bc
Merge: de4b141 6c991aa
Author: Zach Feldman <zachfeldman@gmail.com>
Date:   Tue Nov 25 13:01:54 2014 -0500

    Merge pull request #201 from nycda/classes-page-custom-field-fix
````


---


# Exercise: Getting to know git

- Create a new project folder with at least two files, perhaps `index.html` and `style.css`

- Initialize a new git repository in this folder

- Type a few lines in each file, such as a comment or two

- Make your initial commit

- Make a change to one or both of the files, then make another commit

- Repeat this process starting from scratch a few times to make sure you have it down


---


# Resources

- NYCDA blog post - [create new git repo](http://nycda.com/git)
- Code Academy: [Learn Git](https://www.codecademy.com/en/courses/learn-git)
- TeamTreeHouse: [Git Basics - Getting Started with Git](https://teamtreehouse.com/library/git-basics)
- Roger Dudler: [Git Simple Guide](http://rogerdudler.github.io/git-guide/)
