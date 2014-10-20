---
layout: post
title: "UNIX Shell For Dummies"
published: true
tags: [Shell, UNIX, Bash]
---
Learning a few UNIX commands can be useful. Since it's the 'default' programming language that pops up when you run the Terminal, it's worth knowing a few of the more basic commands:
These are sorted by 'difficulty' - you should know the first ones first.

### Navigation

`cd` - changes the current directory.
eg. `cd ~` - changes where you are to HOME directory
eg. `cd Documents`  - goes one file deeper into the 'Documents' folder
eg. `cd ..` - goes up one directory

`ls` - list files or directories in current directory
eg. `ls -la` - uses the options '-l' (list in detail) and '-a' (show hidden files)

`pwd` - **p**rint **w**orking **d**irectory. Shows where you are (relative to the root folder)

### Copying

`cp` - copy
eg. `cp anchovy.txt fishes/anchovy.txt` - creates a copy of the file under the 'fishes' directory.

`cp -r` - copy recursively. Useful for directories.
eg. `cp -r anchovy fishes/anchovy` - copies all the anchovy-related files from the folder 'anchovy'

### Deleting

`rm` - remove
eg. `rm platypus.txt` - deletes the specified file

`rmdir` - remove directory

### Moving / Renaming

`mv` - move
This works like cp, except it removes the initial file / directory
eg. `mv anchovy.txt fishes/anchovy.txt` - moves & **removes** the file.
Renaming: `mv anchovy.txt sardine.txt`

### Creating Folders

`mkdir` - creates a new directory
eg. `mkdir pelicans`

`mkdir -p` - creates a series of new directories.
eg. `mkdir -p Pelecanidae/Pelicans/Great-White-Pelican`

### Getting help

`man` - find the **man**ual
eg. `man man`
eg. `man pwd`

### Showing files

`cat` - show pure text version of the file.
Con**cat**enates & prints the file
eg. `cat gerbil_name.txt` - simply outputs text: 'Fred'

`less` - outputs text with more features.
Better for larger files. Includes scrolling, searching, etc..
eg. `less encyclopedia.txt` - won't crash & is still useful

`sort` - guess what this one does... go on. I'm not going to tell you.
It's a game.

### Comparing files

`diff` - shows the **diff**erences between two files
eg. `diff red_spotted_woodpecker.txt lesser_woodpecker.txt`

### Finding programs

`whereis`
Useful if you're running the wrong version of ruby. Or something similar.
Provides the location of the executable file.

### Changing File Permissions

`chmod`
I've written a quick primer on UNIX file permissions [here]({% post_url 2014-10-18-unix-permissions.md %})
A common chmod file permission to set is `chmod 755`, which is `rwx` for the Owner but only `rw` for other users.

### Search for text

`grep`
Grep's a fairly big topic.
![Grep Book]({{ site.url }}/assets/grep.jpg)

eg. `grep "some string" filename`
eg. `grep "REGEX" filename`
eg. `grep -i "some string" filename` - case insensitive


## Flags

Flags are optional parameters that you can pass in to a shell command. We've met some already; here're two: `ls -la`. You can see a full list of available options under the `man` page of the commands.
