# intro_to_cli

The terminal is a super useful tool that allows you to interact with your computer in all sorts of ways, from managing files, installing apps, and adjusting system settings. However, since the terminal has a text user interface (TUI), it has a relatively high learning curve compared to tools that have a graphical user interface (GUI). Thus, this repository serves as a short tutorial to help early programmers and computer science students get more comfortable with the terminal. We will explain what the terminal is and teach you how to use it to manage all your files.

Authors: Stevie Kim and Sophie Park

---

## What is the Terminal?

![MacOS Terminal](/assets/macos-terminal.jpg "MacOS Terminal")

As we mentioned before, the terminal, also known as the command-line interface (CLI), is a tool that allows you to execute text commands on your computer. This allows you to interact directly with your operating system, which allows you to do almost anything you want on your computer. In fact, before many modern programming tools like VSCode existed, programmers had to use the terminal to write all their software. To this day, many argue that the terminal is still one of the best tools for programming.

How you access the terminal differs depending on your operating system. On `macOS`, you can access the terminal via the **Terminal** app installed on your device. On `Windows`, you can access the terminal using a couple different applications, mainly **Command Prompt** or **PowerShell**. Finally, on `Linux`, there are many different applications you can use to access the terminal, such as **Konsole, Alacritty, Kitty, GNOME Terminal,** and more. However, chances are that if you are on Linux, it is likely that you already know how to access the terminal using your favorite terminal app, since many Linux distributions depend on the use of the terminal more than macOS and Windows.

## The Basics of Using the Terminal

Let's begin learning how to use the terminal! Whenever you open the terminal app, you start a new terminal session. Here, you will automatically start off in your home folder. It should look something like this:

```
~
```

`~` is the symbol that is used to represent the home folder. When you are using the terminal, you are always in a folder that exists on your device. In fact, you can access every folder on your device through the terminal. Before we can do that, we need to introduce our first few *terminal commands*.

### `pwd`

`pwd` stands for *print working directory* and is a command that prints the location of your current directory. Thus, if we want to see where exactly our home folder lives in our system, we can type `pwd` into the terminal. Hitting enter will confirm the command and should show a result that looks similar to this:

[Insert image of pwd in home folder]: # 

This simple command allows us to determine where we are, which can help us when traversing our file system.

### `ls`

`ls` stands for list and is a command that lists the contents of your current folder. Using this command in the current home folder should look something like this:

[Insert image of ls in home folder]: # 

> Note: The results of using the `ls` command on your own device may look different than this, since you may have different files and folders in your home folder.

This tells us what files and folders exist in our home folder.

### `cd`

We can then move into one of those folders using the `cd` command. `cd` stands for *change directory* and directory is just another word for folder. Thus, the `cd` command changes our location by moving us into another directory/folder.

For example, we can move into the `Downloads` folder using the following command:

```
cd Downloads
```

Then, by calling `ls` again, you should see that your `Downloads` folder has different contents to your `~` directory.


[Insert image of ls in Downloads folder]: # 

The `ls` and `cd` commands are your bread-and-butter. They allow you to traverse the contents of your computer by first listing the contents of your current folder using `ls` and then moving into one of those sub-directories using `cd`. Furthermore, if you ever get lost or need to know the exact location of your current working directory, then you can use `pwd` to print that information out. These three commands give you the basic ability to move through all the files on your computer. We encourage you to practice using these commands and exploring many of the folders currently living on your computer!

##

### something

Commands:
- ls
- cd
- pwd
- mkdir
- touch
- rmdir
- rm
- cat
- nano
- echo
- cp
