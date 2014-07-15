Teaching Command-Line tools
===================

**easy**

- navigate and manipulate the file-system;

<p>These are some of the basic commands required to navigate and manipulate the file-system in the UNIX command-line environment. They all stand for something, which can make it easy to remember. They all also come with documentation built-in using the command line - `man <commandName>`. </p>

<p>I believe it's useful to know what they stand for as it makes the purpose really clear. Also note that most of these also have options you can pass in to get specific things done.</p>

<p>Some definitions before-hand:</p>

```
file system object - such as a file, directory, or link
```

`cat` - concatenate and list files

`cd` - change directory

`chmod` - change mode, change the access permissions to file system objects

`chown` - change owner, change the owner of a file

`chgrp` - change group, change the group associated with a file system object to one of which they are a member

`cksum` 

`cmp` 

`cp` 

`dd` 

`du` 

`df` 

`file` 

`fsck` 

`fuser` 

`ln` 

`ls` - list files in directory

`mkdir` - make directory

`mount` 

`mv` 

`pax` 

`pwd` - print working directory

`rm` 

`rmdir` 

`size` 

`split`

`tee`

`touch`

`type`

`umask`

- compose processes with pipes;
- comfortably edit a file with emacs and vim;
- text processing with awk, grep, sed, etc.
- create, modify and execute a Makefile for a software project;
- write simple shell scripts.

**harder**

- [Find the five folders in a given directory consuming the most space.](http://superuser.com/questions/9847/linux-utility-for-finding-the-largest-files-directories)

largest 10 files

```
find . -type f -print0 | xargs -0 du | sort -n | tail -10 | cut -f2 | xargs -I{} du -sh {}
```

largest 10 directories

```
find . -type d -print0 | xargs -0 du | sort -n | tail -10 | cut -f2 | xargs -I{} du -sh {}
```

The difference is in the type. It is either f, file or d, directory.

- Report duplicate MP3s (by file contents, not file name) on a computer.
- Take a list of names whose first and last names have been lower-cased, and properly recapitalize them.
- Find all words in English that have x as their second letter, and n as their second-to-last.
- Directly route your microphone input over the network to another computer's speaker.
- Replace all spaces in a filename with underscore for a given directory.
- Report the last ten errant accesses to the web server coming from a specific IP address.

**resources and reading**

- [What every computer science major should know](http://matt.might.net/articles/what-cs-majors-should-know)
- [Command-line interface](http://en.wikipedia.org/wiki/Command-line_interface)
- [Shell built-in](http://en.wikipedia.org/wiki/Shell_builtin)
- [Unix Commands](http://en.wikipedia.org/wiki/Template:Unix_commands)
