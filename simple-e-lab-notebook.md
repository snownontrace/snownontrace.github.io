---
layout: protocols
title: A simple electronic lab notebook using Markdown and Git
author: Shaohe Wang
author_url: https://shaohewanglab.org
date: 2022-12-16
---

The most commonly used elements in a lab notebook are text, tables and images, which can be easily organized in Markdown files. This can be greatly facilitated by a modern text editor, such as **Visual Studio Code**. The most important feature of an electronic lab notebook is to trace editing history, which can be conveniently achieved by **Git**.

### 1. Use Markdown to organize text, tables and images

* Learn markdown basics [here](https://www.markdownguide.org/basic-syntax/).

* Practice markdown following [this tutorial](https://www.markdowntutorial.com/).

* Use Markdown to make a table:

  ```Markdown
  | Col 1 (left aligned) | Col 2 (center aligned) | Col 3 (right aligned) |
  |:---|:---:|---:|
  | aa | ab | ac |
  | ba | bb | bc |
  | ca | cb | cc |
  ```

  The rendered output looks like this:

  | Col 1 (left aligned) | Col 2 (center aligned) | Col 3 (right aligned) |
  |:---|:---:|---:|
  | aa | ab | ac |
  | ba | bb | bc |
  | ca | cb | cc |

* Use Markdown to link an image (or any other files):

  ```Markdown
  ![image alt text (displays when image fails to load)](/path/to/image.png)
  ```


* It is highly recommended to use a modern text editor, such as the [Visual Studio Code (VS Code)](https://code.visualstudio.com/), to facilitate markdown editing.
  * For example, in VS Code, you can drag a picture (or any other file) into the markdown file while holding the `Shift` key to insert the formatted text.
  * There are also many -- probably too many -- choices of extensions for markdown. I have been using "Markdown All in One," "Markdown PDF," "markdownlint," and "Selection Word Count."

### 2. Use Git and GitHub for version control and cloud backup

If you are new to Git, I highly recommend [the Software Carpentry Lesson for Git](https://swcarpentry.github.io/git-novice/index.html). Specifically, you can:

* Learn basic concepts of Git [here](https://swcarpentry.github.io/git-novice/01-basics/index.html).

* Install Git.
  * If you are using a new Mac, you probably have a quite new version of Git installed. Check by typing `git --version` in your terminal. If the version number is close to [the current version](https://git-scm.com/downloads), you can just use the pre-installed version.
  * Otherwise, follow instructions [here](https://carpentries.github.io/workshop-template/#git) to install Git on Windows, Mac or Linux systems.

* [Set up Git](https://swcarpentry.github.io/git-novice/02-setup/index.html) on your computer.

* [Use GitHub](https://swcarpentry.github.io/git-novice/07-github/index.html) for cloud backup.
  * It is recommended to use [SSH connections](https://docs.github.com/en/authentication/connecting-to-github-with-ssh).

* If you are using VS Code, you could easily commit and sync changes within the VS Code interface. If it keeps asking for the SSH passphrase, you can open a terminal window and run `ssh-add`, which will ask for the SSH passphrase once and VS Code should no longer ask for it.
