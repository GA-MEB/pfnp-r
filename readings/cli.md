[![General Assembly Logo](https://camo.githubusercontent.com/1a91b05b8f4d44b5bbfb83abac2b0996d8e26c92/687474703a2f2f692e696d6775722e636f6d2f6b6538555354712e706e67)](https://generalassemb.ly/)

# Reading : Use a Command Line Interface

Back before people navigated their computers with mice, but after they had
largely phased out punchcards as the way of writing computer programs,
developers largely communicated with their computers through a text-based
interface called a **command line interface**, or **CLI**.
Many of the great developments in the history of computers were made during
this time, including the invention of things like operating systems,
so it's not so surprising that this legacy has lived on.
To this day, most developers will use a terminal interface (such as `Terminal`
on OS X) as one of the primary ways of working with their code.
These terminals typically run a program like `bash` or `zsh` to handle the
actual interaction of reading text commands and running code.

Since this interface existed before windows and clicking, developers needed
other ways of accomplishing everyday tasks, like moving around, viewing the
contents of directories, and creating/moving/deleting files and directories
by typing text commands into the terminal. Here's a quick reference of these
basic terminal commands.

| Behavior                      | Command                                                   |
|-------------------------------|-----------------------------------------------------------|
| Show current location         | `pwd` (present working directory)                         |
| Move to some location         | `cd` + path to directory                                  |
| List contents of directory    | `ls` + path to directory                                  |
| Create new directory          | `mkdir` + name                                            |
| Create new file               | `touch` + name                                            |
| Move or rename file/directory | `mv` + current path to file/directory + new path/location |
| Delete a file/directory       | `rm` (`rm -r` for directory) + path to file/directory     |

> WARNING : Misuse of `rm -r`, 'recursive delete',
> can potentially 'brick' your computer
> (especially in combination with `-f`, or 'force').
> PLEASE USE WITH CAUTION.
