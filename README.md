# Git Practice
This repository was created to implement the practice from the course Git & Github Profesional by [Platzi](https://platzi.com/clases/git-github/). Here, I'll provide with a list of the ten most resourceful commands with this version control system*.

## *The Swiss Army Knife for Git&GitHub*

* git-clone - Clone a repository into a new directory
  * synopsis
  ```
    git clone [--template=<template_directory>]
      [-l] [-s] [--no-hardlinks] [-q] [-n] [--bare] [--mirror]
      [-o <name>] [-b <name>] [-u <upload-pack>] [--reference <repository>]
      [--dissociate] [--separate-git-dir <git dir>]
      [--depth <depth>] [--[no-]single-branch] [--no-tags]
      [--recurse-submodules[=<pathspec>]] [--[no-]shallow-submodules]
      [--[no-]remote-submodules] [--jobs <n>] [--sparse] [--[no-]reject-shallow]
      [--filter=<filter>] [--] <repository>
      [<directory>]
  ```
  
  * example
  ```
      $ git clone git://git.kernel.org/pub/scm/.../linux.git my-linux
      $ cd my-linux
      $ make
  ```

* git-status - Show the working tree status
  * synopsis
  ```
  git status [<options>…​] [--] [<pathspec>…​]
  ```

* git-fetch - Download objects and refs from another repository
  * synopsis
  ```
  git fetch [<options>] [<repository> [<refspec>…​]]
  git fetch [<options>] <group>
  git fetch --multiple [<options>] [(<repository> | <group>)…​]
  git fetch --all [<options>]
  ```
  
  * example
  ```
  $ git fetch origin
  ```

* git-add - Add file contents to the index
  * synopsis
  ```
  git add [--verbose | -v] [--dry-run | -n] [--force | -f] [--interactive | -i] [--patch | -p]
    [--edit | -e] [--[no-]all | --[no-]ignore-removal | [--update | -u]]
    [--intent-to-add | -N] [--refresh] [--ignore-errors] [--ignore-missing] [--renormalize]
    [--chmod=(+|-)x] [--pathspec-from-file=<file> [--pathspec-file-nul]]
    [--] [<pathspec>…​]
  ```
 
  * example
  ```
  $ git add Documentation/\*.txt
  $ git add git-*.sh
  ```
 
* git-commit - Record changes to the repository
  * synopsis
  ```
  git commit [-a | --interactive | --patch] [-s] [-v] [-u<mode>] [--amend]
	   [--dry-run] [(-c | -C | --squash) <commit> | --fixup [(amend|reword):]<commit>)]
	   [-F <file> | -m <msg>] [--reset-author] [--allow-empty]
	   [--allow-empty-message] [--no-verify] [-e] [--author=<author>]
	   [--date=<date>] [--cleanup=<mode>] [--[no-]status]
	   [-i | -o] [--pathspec-from-file=<file> [--pathspec-file-nul]]
	   [(--trailer <token>[(=|:)<value>])…​] [-S[<keyid>]]
	   [--] [<pathspec>…​]
  ```
  
  * example
  ```
  $ edit hello.c
  $ git rm goodbye.c
  $ git add hello.c
  $ git commit
  ```
  
* git-push - Update remote refs along with associated objects
  * synopsis
  ```
  git push [--all | --mirror | --tags] [--follow-tags] [--atomic] [-n | --dry-run] [--receive-pack=<git-receive-pack>]
	   [--repo=<repository>] [-f | --force] [-d | --delete] [--prune] [-v | --verbose]
	   [-u | --set-upstream] [-o <string> | --push-option=<string>]
	   [--[no-]signed|--signed=(true|false|if-asked)]
	   [--force-with-lease[=<refname>[:<expect>]] [--force-if-includes]]
	   [--no-verify] [<repository> [<refspec>…​]]
  ```
  
  * example
  ```
  $ git push origin master
  ```
  
* git-pull - Fetch from and integrate with another repository or a local branch
  * synopsis
  ```
  git pull [<options>] [<repository> [<refspec>…​]]
  ```
  
  * example

  ```
  $ git pull
  $ git pull origin
  $ git pull origin next
  ```
  
* git-merge - Join two or more development histories together
  * synopsis
  ```
  git merge [-n] [--stat] [--no-commit] [--squash] [--[no-]edit]
   [--no-verify] [-s <strategy>] [-X <strategy-option>] [-S[<keyid>]]
   [--[no-]allow-unrelated-histories]
   [--[no-]rerere-autoupdate] [-m <msg>] [-F <file>] [<commit>…​]
  git merge (--continue | --abort | --quit)
  ```
  
  * example
  ```
  $ git merge fixes enhancements
  $ git merge -s ours obsolete
  $ git merge --no-commit maint
  ```
  
* git-stash - Stash the changes in a dirty working directory away
  * synopsis
  ```
  git stash list [<log-options>]
  git stash show [-u|--include-untracked|--only-untracked] [<diff-options>] [<stash>]
  git stash drop [-q|--quiet] [<stash>]
  git stash ( pop | apply ) [--index] [-q|--quiet] [<stash>]
  git stash branch <branchname> [<stash>]
  git stash [push [-p|--patch] [-k|--[no-]keep-index] [-q|--quiet]
        [-u|--include-untracked] [-a|--all] [-m|--message <message>]
        [--pathspec-from-file=<file> [--pathspec-file-nul]]
        [--] [<pathspec>…​]]
  git stash clear
  git stash create [<message>]
  git stash store [-m|--message <message>] [-q|--quiet] <commit>
  ```
  
  * example
  ```
  $ git pull
  ...
  file foobar not up to date, cannot merge.
  $ git stash
  $ git pull
  $ git stash pop
  ```
* git-reset - Reset current HEAD to the specified state
  * synopsis
  ```
  git reset [-q] [<tree-ish>] [--] <pathspec>…​
  git reset [-q] [--pathspec-from-file=<file> [--pathspec-file-nul]] [<tree-ish>]
  git reset (--patch | -p) [<tree-ish>] [--] [<pathspec>…​]
  git reset [--soft | --mixed [-N] | --hard | --merge | --keep] [-q] [<commit>]
  ```
  * example
  ```
  $ git commit ...
  $ git reset --soft HEAD^      
  $ edit                        
  $ git commit -a -c ORIG_HEAD 
  ```
  
\* For full guiadance about the use of these commands, visit the [Git documentation](https://git-scm.com/doc).
  


