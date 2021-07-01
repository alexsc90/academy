# Git Practice
This repository was created to implement the practice from the course Git & Github Profesional by [Platzi](https://platzi.com/clases/git-github/).

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

\* For full guiadance about the use of these commands, visit the [Git documentation](https://git-scm.com/doc).
  


