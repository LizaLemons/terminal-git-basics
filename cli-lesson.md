
# Command Line Interface

---


### Lesson Objectives:
- Differentiate between a GRAPHICAL USER INTERFACE (GUI) and COMMAND LINE INTERFACE (CLI)
- Explain the 3 reasons the CLI is better for developers than the GUI
- Make changes from the CLI
- Name the parts of the command line prompt
- Describe ABSOLUTE vs. RELATIVE path
- Define WORKING DIRECTORY


---


### Context: why do I need to know about the COMMAND LINE
All of you learned about tools like Command Line during the prework, but we're going to review these concepts because they are crucial to developers.

These are skills we absolutely expect you to master during the class. You will use them to turn in homework on a daily basis and you will use them daily at your jobs.


---

### Intro - What is the Command line?
One of the most basic tools in every day developer life is the COMMAND LINE. The CLI is the way developers interface with their computers. What do I mean by that? I mean it's the way you make your computer do simple tasks, such as creating or deleting a file, and more complex tasks, like compiling code. The concept is simple: you type a command into the COMMAND LINE and the computer executes it.


---


#### GUI
- Open a Finder window and move around the file system, create folder + file on desktop
- This Finder window is what is meant by GUI! It's as simple as that.
- But why is it called a GUI, why does it have a name at all?!
- Before 1960s the GUI didn't exist, there was only the Terminal. The GUI is easier for non-techies to use.


---


#### File structure
- *Draw on the board: structure of the computer (up to that specific file)*
- Root (/) ---> Users, Applications, etc. ---> LizaRamo (home, ~) ---> Desktop, Downloads, Music, Pics, etc.
- Important shortcuts: root (/) & home (~)
- CD around


---


#### GUI vs. COMMAND LINE
- Remember when we created a new folder using the GUI? Now let's do that using the CLI
- Use Spotlight to open TERMINAL
- Navigate to the same file as in GUI side by side
- We can use the CLI to get to the same file.

But why should we learn to use the COMMAND LINE when we could just use the GUI?
1. The CLI is faster
1. It's the professional way to do things as a developer
1. There are some things you can only do from the CLI


---


#### Parts of the COMMAND LINE prompt:
```bash
lizaramo ~/Desktop/puppy-pics
$    #this is where your command will go
```

Structure:
- Name of your computer | Working directory | branch (if repo) | $Command
- working directory?


---


#### Working directory
- Simplest definition: where you are in the file system
- Memorize this: `pwd` ---> this command tells you where you are within the file system
- `~/Desktop/puppy-pics`


---


#### Navigating: Relative and Absolute Paths
- Let's go back to the file structure drawing
- Let's say you're in the `desktop` in the CLI. How do we get from here to the directory: `puppy-pics`
- We need to find out that directory's `path`. Is that directory on the desktop, or buried within 3 other directories?
- `./fun/animals/puppies/puppy-pics`
- But what if we don't know where you are? We can use the absolute path using one of the shortcuts `/` or `~`.
- From the root directory, our path is: `cd /Users/LizaRamo/Desktop/fun/animals/puppies/puppy-pics`
- From our home directory, our path is: `cd ~/Desktop/fun/animals/puppies/puppy-pics`


---


### Takeaway: Relative vs. Absolute Paths

**Absolute:** These paths will begin with either `/` or `~`. For example:

```
$ /Users/LizaRamo/Desktop/puppy-pics
```

or

```
$ ~/Desktop/puppy-pics
```


**Relative:** These paths will begin with the name of a directory or a file.

```
$ puppy-pics/cute-pic-1.png
```


---


#### What's in a name

*Let's pause for a moment to talk about terms.*

- Don't get confused by the terminology: CLI, command line, Terminal, shell, console, etc.
- For now, use all of these interchangeably.
- **CLI:** Command Line Interface
- **Terminal:** name of Apple's CLI app


---


#### Let's Talk About Some Common Commands


---


### Print Working Dir - pwd

```
$ pwd
```

This will print your *working directory*, or the folder where you are currently located.


---


### LS

```
$ ls
```

List contents of a directory.


---


### CD

```
$ cd <path to directory>
```

**Change Directory**. This allows us to move up and down the file system.


---


### Single Dot

The single dot represents your **current directory.** You can use it in conjunction with several commands, most notably `ls` and `cd`.

```
$ cd .
```

You'll stay in the same place! Ha.

```
$ ls .
```

List contents of the current directory.


---


### Double Dot

The double dots represent the **directory above the current one** in the file structure tree.

We use this often with `cd`.

```
$ cd ..
```

This will take you one folder above your current one.


---


### Make Directory

```
$ mkdir <name of new directory>
```

This commands creates a new folder, or directory, in the specified location.


---


### Touch

```
$ touch <name of new file>
```

This commands creates a new file in the specified location.


---


### Copy

```
$ cp <source file> <destination of the duplicate>
```

This command allows you to copy, or make a duplicate, of a file.

Alternately, if you'd like to copy a directory, you must use the `-r` flag, which stands for `recursive`, meaning all of the contents inside the directory.

```
$ cp -r <source file> <destination of the duplicate>
```


---


### Move

```
$ mv <current location> <new destination>
```

Unlike **copy**, **move** does not duplicate the file or directory, it simply moves it to a new location.


---


### Remove

**Be careful**. This is permanent.

```
$ rm <name of file>
```

If you'd like to remove a directory, you must supply the `-r` flag.

```
$ rm -r <name of file>
```


---


#### You do: exercise on your own (10 mins)
*Don't touch your mouse, don't use the GUI*
- Create a directory on your desktop called `my-folder`
- Change into that directory
- Print your current location
- Create a file in your directory called `my-file.html`
- Create a `markdown` file called `my-second-file.md`
- List all the files in your directory
- Move `my-file.html` to your desktop
- Copy `my-second-file.md` to the desktop
- Delete `my-file.html`


---


### Tips


---


### Tip 1: Re-entering commands

Just press up in your terminal!


---


### Tip 2: Use tab to autocomplete file & folder names

When you are `cd`-ing into a directory, you can type in the first few letters of the file, then press tab to see if it will autocomplete the name of the file!


---


#### Further reading:

- [Learn Command Line the Hard Way](http://cli.learncodethehardway.org/book/)
- [Command Line Tutorial](http://www.davidbaumgold.com/tutorials/command-line/)
