# Revisions and the Cloud reading notes

## What's Git?

- Git is a Distributed Version control system (DVCS) which directly tracks changes to the data in file system.
- A file system or directory tree being tracked by git is refered to as a repository.
- Git tracks changes with commits
  - A commit is a snapshot of the changes being made.
  - Collectively, all the commits on a repository represent change history of that repository.
- Git relies primarily on local operations allowing offline and potentially faster work.
- Git can detect file corruption and loss of information which occur during operation.
- With the above features and others not covered for the sake of brevity, Git as a system is very resilient to loss of data.

## What can I do with Git?

- Git is available on all major operating systems (Windows/Mac OS X/Linux)
  - Git is often paired with or installed with GitHub. GitHub is a service for hosting Git repositories online, and a very popular one at that.
- Your name and email should be configured into Git, as this info will be signed onto every commit.
  - `git config --global user.name "Your Name"` sets your name
  - `git config --global user.email "example@email.com"` sets your email

### Setting up a Git Repository

1. A Git repository's life starts with the command `git init` being performed on a project's root directory.
2. Then enter the following commands into the terminal.
    - `git add *.c` 
    - `git add LICENSE`
    - `git commit -m "Initial commit"`

### Cloning

- With `git clone "url"` you can copy a repository from a remote location (web service, LAN server, etc).

- Upon making commits to a cloned repository `git push origin main` will upload the commits to the corresponding remote repository. The alias `origin` is the destination of this operation and `main` is the source of the operation.

### Local Repository Structure

- The local Git Repository contains the following essential components:
  - Working Directory, which is where the actual files reside
  - Index, which used for staging
  - Head, which points to the latest commit.

### File Life Cycle

Files tracked in a Git repository can either be committed, modified, or staged. Additionally, when new files are created, they are untracked and must be introduced with `git add` into the commit-modify-stage cycle.

- I just created a project file named `myprojectfile.txt` in my Git repository. Git automatically flags it as an untracked file. This can be checked with the `git status` command.
- The command `git add "myprojectfile.txt"`  will track the file AND stage it, so it's ready to be committed.
- The command `git commit -m "Commit desc."` will commit the staged changes, thus creating a new snapshot of my repository.

#### Pushing files

- When you wish to sync up the changes done locally with a clone/remote repository, use the `git push` command as explained previously in the cloning section of these notes.
