# intro_to_cli

The terminal is a super useful tool that allows you to interact with your computer in all sorts of ways, from managing files, installing apps, and adjusting system settings. However, since the terminal has a text user interface (TUI), it has a relatively high learning curve compared to tools that have a graphical user interface (GUI). Thus, this repository serves as a short tutorial to help early programmers and computer science students get more comfortable with the terminal. We will explain what the terminal is and teach you how to use it to manage all your files.

Authors: Stevie Kim and Sophie Park

---

## What is the Terminal?

![MacOS Terminal](/assets/macos-terminal.jpg "MacOS Terminal")

As we mentioned before, the terminal, also known as the command-line interface (CLI), is a tool that allows you to execute text commands on your computer. This allows you to interact directly with your operating system, which allows you to do almost anything you want on your computer. In fact, before many modern programming tools like VSCode existed, programmers had to use the terminal to write all their software. To this day, many argue that the terminal is still one of the best tools for programming.

How you access the terminal differs depending on your operating system. On `macOS`, you can access the terminal via the **Terminal** app installed on your device. On `Windows`, you can access the terminal using a couple different applications, mainly **Command Prompt** or **PowerShell**. Finally, on `Linux`, there are many different applications you can use to access the terminal, such as **Konsole, Alacritty, Kitty, GNOME Terminal,** and more. However, chances are that if you are on Linux, it is likely that you already know how to access the terminal using your favorite terminal app, since many Linux distributions depend on the use of the terminal more than macOS and Windows.

## Navigating Files and Folders Using the Terminal

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

`ls` stands for *list* and is a command that lists the contents of your current folder. Using this command in the current home folder should look something like this:

[Insert image of ls in home folder]: # 

> Note: The results of using the `ls` command on your own device may look different than this, since you may have different files and folders in your home folder.

This tells us what files and folders exist in our home folder.

### `cd`

We can then move into one of those folders using the `cd` command. `cd` stands for *change directory* and directory is just another word for folder. Thus, the `cd` command changes our location by moving us into another directory/folder. It takes a single argument as input, which is the name of the directory that you would like to move to. 

For example, we can move into the `Downloads` folder using the following command:

```
cd Downloads
```

> Note: You can only `cd` into directories that exist in your current working directory. To figure out what those directories are, use the `ls` command!

Then, by calling `ls` again, you should see that your `Downloads` folder has different contents to your `~` directory.

This allows us to move deeper into our file system. However, what if we want to move our of our current working directory?

We can do this by passing in `../` as our argument for `cd`. 

```
cd ../
```

Call `ls` again to confirm that you have moved from the `Downloads` folder into your home directory.

[Insert image of ls in Downloads folder]: # 

The `ls` and `cd` commands are your bread-and-butter. They allow you to traverse the contents of your computer by first listing the contents of your current folder using `ls` and then moving into one of those sub-directories using `cd`. Furthermore, if you ever get lost or need to know the exact location of your current working directory, then you can use `pwd` to print that information out. These three commands give you the basic ability to move through all the files on your computer. We encourage you to practice using these commands and exploring many of the folders currently living on your computer!

## Creating Files and Folders

Since we now know how to move through our file system, let's go over ways to create new files and folders.

### `mkdir`

`mkdir` stands for *make directory* and does exactly what it's name suggests: it makes a directory within your current working directory.

Let's use this command to make a folder where we can practice using the terminal!

First, if you are not in your home folder, let's move there using this command:

```
cd ~
```

> Note: As mentioned before, normally, you can only `cd` into folders that exist in your current working directory. However, the home directory `~` is an exception to this, as you can move into this folder no matter where you are on your computer.

Now, let's use `mkdir` to create a folder titled `intro_to_cli`! Like `cd`, `mkdir` takes in one argument, which is the name of the directory you are making. Thus, we can create this folder using this command:

```
mkdir intro_to_cli
```

To check that this folder now exists, use the `ls` command. You should see this folder show up in the output list.

Finally, `cd` into this directory.

### `touch`

`touch` is a command that allows us to create files. Like `mkdir`, it takes in one argument, which is the name of the file you are making.

Let's make a file titled `test.txt`! We can do this using the following command:

```
touch test.txt
```

Now, call `ls` to verify that this file now exists in our working directory.

## Removing Files and Folders

Just as we learned to make files and folders, there are also commands that allow us to remove both files and folders.

### `rm`

`rm` stands for *remove* and allows you to remove files.

To try this out, let's remove the `test.txt` file we just created, using this command:

```
rm test.txt
```

As usual, use `ls` to confirm that this file was deleted.

### `rmdir`

`rmdir` stands for *remove directory* and does the opposite of what `mkdir` does: it removes a directory.

Let's test this our by creating and removing a new directory called `test`.

```
mkdir test
ls
rmdir test
ls
```

We first call `mkdir` to create the directory, use `ls` to check that its there, and then call `rmdir` to remove it. One last call to `ls` lets us verify that we have successfully removed the directory.

## Managing Files (Read, Write, and Copy)

Now that we can create and remove files, let's now learn how to read, write, and copy these files.

### `cat`

`cat` stands for *concatenate*, since it's original purpose was to combine multiple files together into one. However, it is also used to both read and write to files.

Type the following command into the terminal:

```
cat > hello_world.txt
```

Notice that rather the command doesn't terminate and leaves you stuck in an empty line. In this empty line, type in `Hello world!`. Then, hit `Ctrl-D`.

Now, your command should have finished! Furthermore, if you use `ls`, you should notice that we have a new file, conveniently titled `hello_world.txt` in your working directory.

What `cat > hello_world.txt` did was create a new file named `hello_world.txt` in our current directory. However, unlike `touch`, it gave us an opportunity to input text into the file before creating it. This was done when we saw the empty line and entered in `Hello world!`. Finally, entering `Ctrl-D` finished the command.

We just verified that we created the file, but how can we read the contents of this file? Well, we can also use `cat` for this as well! Type in the following command:

```
cat hello_world.txt
```

You should see the following:

[Insert image of our output of hello_world.txt]: # 

This command just printed the contents of our file! Thus, we can use `cat` to both write to new files and read the contents of existing files!

Interestingly enough, the `cat` command can do a lot more. However, we will go over just one more function of `cat`, which is to writing to existing files. We can do this as such:

```
cat >> hello_world.txt
```

Notice that this operation uses `>>` instead of our original `>`. This command allows us to append text to existing files.

Notice that it also opens up an empty line for us to input text. Type in `Hello, world, it's me, [Insert Your Name Here]!` and confirm this command using `Ctrl-D`.

Finally, confirm that this edited the file by running the same command as before:

```
cat hello_world.txt
```

### `nano`

So `cat` is good to adding text to new or existing files, but what about deleting text? What about adjusting files completely? Editing tasks as a whole can require more robust tools, which is exactly what `nano` allows us to do. `nano` opens the *nano text editor*, which is a terminal application that can edit files. Think of it as an extremely simple version of `VSCode`.

Let's use `nano` to adjust the text on `hello_world.txt`:

```
nano hello_world.txt
```

This will open the nano text editor and you should be able to edit the file like many other text editors. You can move your cursor using the arrow keys and add/delete text as you wish. Make some edits to the file (whatever edits you wish) and then save these changes using `Ctrl O` followed by `Enter`. Finally, exit nano using `Ctrl X`. 

Unlike `cat`, `nano` is a fully fledged text editor that gives us a better ability to edit files, without neeeding to leave the terminal. This is one example of the many powerful commands that makes the terminal such an incredible tool. Other text editors that people use through the terminal include `Vim` and `Emacs` and even serve as popular alternatives to `VSCode`. We recommend that you explore those tools, since they are incredibly powerful and convenient to use, especially with programming.

### `cp`

One very convenient command is `cp`, which stands for *copy*. This command allows you to copy one file and place it in a different directory. It takes two arguments: (1) the path to the file you want to copy, and (2) the path to the destination you want to place it in. A *path* is used to describe the location of a file or directory and is a term that shows up a lot in programming and using the terminal.

To showcase how to use `cp`, let's copy our `hello_world.txt` file!

Let's run the following command:

```
cp hello_world.txt hello_world_copy.txt
```

Running `ls` and `cat > hello_world_copy.txt` should confirm that we have successfully duplicated `hello_world.txt` under a different name.

What get's interesting is that we can do this same command from any starting directory, as long as we adjust our path to match. Say, for example, I `cd` back out to our home directory using:

```
cd ../
```

By adjusting the paths of both arguments for this command, I can run basically the same command from here:

```
cd intro_to_cli/hello_world.txt intro_to_cli/hello_world_copy2.txt
```

> Note: Since we are back in the home directory, the `hello_world.txt` file doesn't live in this folder directly. Rather, it lives inside the `intro_to_cli` folder that lives in the home directory. Thus, to copy this file, we need to specify that it lives in `intro_to_cli` by augmenting its path to be `intro_to_cli/hello_world.txt`. The same goes for the name of our duplicate file, `hello_world_copy2.txt`.

We can then `cd` back into `intro_to_cli` and verify that this duplicate file exists using `ls` and `cat`.

### `mv`

One final command that I would like to review is `mv`. This allows us to both *move* and *rename* existing files. 

Say we make a new folder named `temp` inside `intro_to_cli`.

We can move our `hello_world.txt` file inside this new folder `temp` by using the following command:

```
mv hello_world.txt temp/hello_world.txt
```

This command moves our `hello_world.txt` file into the `temp` folder while keeping its name. As always, check to see that this command was successful using `cd` and `ls`.

We can undo this command by swapping the source and destination paths:

```
mv temp/hello_world.txt hello_world.txt
```

Furthermore, we can rename files by changing the name of the file in the destination:

```
mv hello_world.txt hello_world_changed.txt
```

We can combine these concepts to move a file and rename it at the same time:

```
mv hello_world_changed.txt temp/hello_world.txt
```

As always, verify that each of these commands worked using the `cd` and `ls` commands.

## Wrap Up

Through this short tutorial, we reviewed how to open and use the terminal to manage the files on your device. Managing your files is a skill that will always come into play whenever you are performing any task on your computer, which is why we prioritized teaching these skills. Additionally, see the file [activities.md](https://github.com/sjkim994/intro_to_cli/blob/main/activities.md) for some additional challenges that will further hone your terminal skills. We hope you learned something and that you feel more comfortable using the terminal!
