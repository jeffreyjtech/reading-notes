# Prework - The Command Line

## Notes

### ***The Command Line***:

- I've known about the command line for most of my life but I did not know what a shell really is. It's good to know the difference. The terminal is an ultra-generic concept and a basic part of any OS, but the shell tells you what flavor of terminal you'll be interacting with. I also didn't know that `echo` is a command to display messages.

### ***Basic Navigation***:

- It's crazy how many options there are for something as simple as `ls`. Also the meta-data that appears when using `ls -l` is very interesting. Super technical stuff I'm sure but it's always neat to see the nuts-and-bolts of a file system.
- I wish I knew 3 months ago that `cd` with no args moves you to the home directory.
- Thankfully as a 201 and 301 graduate I already know what the essential function of `pwd`, `ls`, and `cd`. I will reiterate them anyways:
  - `pwd` - Prints the path of the working directory.
  - `ls` - Prints the contents of a directory.
  - `cd` - Changes the working directory.

### ***More About Files***

- Linux's file system being an extension-less system gives me some questions. How else besides the file extension does Linux know what a file is? Is there, like, a schema registry or special "file headers" which instruct Linux on what something is? Or is it as simple as the user being trusted to use the correct programs to open a certain type of file?
  - I realize the last possibility I suggested isn't viable since `file` tells you a file's type.
- With spaces being special characters in CLIs, I can now see why spaces are avoided in file names for coding projects.

### ***Manual Pages***

- Once again, Linux continues to be exceedingly clever while also being dumb from a UX perspective. This very assignment just taught me how to find keywords in manuals and what the right command is for finding manuals in the first place. I've been using `help` this whole time! I'll try to use `man -k` and `/term` to do find more useful info, too.

### ***File Manipulation***

- I guess I can use `rmdir` in the future instead of `rm -r`, although the former seems less useful since the directory has to be empty.
- The real use of the `touch` command is interesting. I can totally see how modifying the apparent access/modify times on a file is useful. That said it's most common use for creating blank files is yet another feature of Linux that I don't like from a UX perspective.

### ***Cheat Sheet***

I'll just list the commands/options/wildcards I want to remember from this sheet which I don't already know

- `?` is a single character wildcard
- `[]` is a range of wildcards characters.
- `du` finds disk usage.
- `df` find the file system's disk usage
- Linux has processes like any OS.
  - They can be printed in different contexts with `jobs` and `ps`
  - They can be killed with `kill`
    - They can be extra-killed with `kill -9`
  - They can be paused with **CTRL-Z**
  - They can be moved from the background to the foreground with `fg`.
