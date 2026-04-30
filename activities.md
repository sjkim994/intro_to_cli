# Activities!!!
Here are some activities to help your learning.

### Here's the tutorial video again for your convenience

[![Watch the video](https://img.youtube.com/vi/0GL0FfJYOYs/default.jpg)](https://youtu.be/0GL0FfJYOYs)


## Challenge 00
What is your present working directory? Find out by doing the command `pwd`.

## Challenge 01
*List* out all the contents inside the folder/directory you're currently in. `ls` = list.

## Challenge 02
Make a file with the `touch` command. Try running `touch test.txt`.

## Challenge 03
Confirm that there is a new file with `ls`.

## Challenge 04
Let's remove the file you just created. Run `rm test.txt`

Then run `ls` to confirm the file has been deleted.

## Challenge 05
Run `touch wow.txt`. Run `ls` to confirm the new file exists, then run `nano wow.txt`. This should pop up a terminal-based text editor. Add a few lines of text/anything you want, then save and exit back to the terminal.

## Challenge 06
Run `cat wow.txt`. This should print out the text content that you put in the file in the previous challenge.

## Challenge 04
I'm going to try to teach you two things in this challenge. The first new thing is that pressing `tab` autofills the names of files as you type them. The second new thing is that you can move through your command history by pressing the up and down arrows on your keyboard.

In the following order:
1. Try `touch teester.txt`
2. Try `ls`
3. Type out `rm teest` and then press `tab` on your keyboard. Assuming that there's no other objects in your pwd that start with "teest", the filename `teester.txt` should automatically fill in. If there's multiple files that start with "teest", then pressing `tab` will print all the files that start with "teest".
4. Delete the `teest.txt` file
5. Press the up arrow on your keyboard. This should send you to the previous command you did. Keep pressing up until you get to `ls`, and then press enter to confirm that the file has been deleted. You can also press the down arrow to go forward in your command history.

(p.s. you can see your history by typing `history` and you can clear your history by typing `history -c`)

## Challenge 04
Move backwards/upstream in the file directory by typing `cd ..`


# Congratulations!!! You are now a TERMINAL MASTER!!!


### Secret awesome bonus challenge 1
Try adding the `-a` modifier to the `ls` command so that it'll print *a*ll files+directories, including the hidden stuff!! `-a` stands for *a*ll!! Does the output of `ls -a` look any different from the output of just `ls`?

p.s. Modifiers are generally in the format of `com -m`, where `com` is a stand in for any command in general and `-m` is a one or two-letter long modifier. For example, `ls -h` adds the `-h`, or "help" modifier. Adding `-h` to the end of any command will, in general, return an abridged version of its documentation.

### Secret awesome bonus challenge 2
If you did challenge 01.01 correctly, you should see two periods `..` at the top of the list. Try typing `cd ..`. Did you change directory? Where are you now? Considering your new location, what do you think `cd` stands for?

p.s. for a bonus, look int owhy we often use `./` at the start of files.

### Secret awesome bonus challenge 3
Try `ls -l` and then `ls -al`. How do these two differ from `ls -a`?

p.s. What do you think `-l` stands for?

As a bonus, you can try figuring out

### Secret awesome bonus challenge 4
Look up `sudo rm -rf /` in your browser. It's a meme. But it also has academic value because we can piece it apart to find out what it means.

`sudo` is a portmaneu of `superuser do`, 

`r` is for recursive, and `f` is for ___

And `/` in this context means ___
