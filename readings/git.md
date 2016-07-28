[![General Assembly Logo](https://camo.githubusercontent.com/1a91b05b8f4d44b5bbfb83abac2b0996d8e26c92/687474703a2f2f692e696d6775722e636f6d2f6b6538555354712e706e67)](https://generalassemb.ly/)

# Reading : Save Work with Git

**Git** is a tool invented by the father of Linux, Linus Torvalds,
who decided that existing tools for version control (the process of keeping
track of changes to a project) _just weren't good enough_.
Git is 'distributed' -- it has no central "master record" for the state of a
project. This may seem like a weakness, but it's actually a strength, since it
allows for large numbers of people to easily work on the same project without
interfering (or even interacting) with each other.

Git does this by letting people **clone**, or copy, the entirety of a given
version of a project into some new location. The Git project (known as a
**repository**; **repo** for short) tracks all changes made to each and every
file inside it. These changes can then be compared to the history of changes
recorded in another repo, and it can be determined whether all of those changes
can be successfully integrated.

To turn a directory into a Git repository, `cd` into the directory and run the
command `git init`. This will create a hidden directory called `.git`, which you
can see by typing `ls -a`.

At this point, you can type `git status` to see a report on the state of your
repo. Before **committing** (think 'saving') a set of changes to the repo,
you'll need to choose which changes to include; this is done through the
`git add` command. `git add someFile.txt` will take all changes in someFile.txt
that have been made since the last commit record and select them for including
in the next one. These changes are referred to as being 'staged'; to 'unstage'
those changes, replace `add` with `reset` (i.e. `git reset someFile.txt`).

Once you've selected the files you want to include, type `git commit`; this will
take you to a text editor window where you can write a detailed message
describing the changes you make. You can see the full history of these messages
by typing `git log`.

There are many other useful features to Git, but these are the only ones we'll
be focusing on right now.
