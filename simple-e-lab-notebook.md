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
  | :--- | :---: | ---: |
  | aa | ab | ac |
  | ba | bb | bc |
  | ca | cb | cc |
  ```

  The rendered output looks like this:

  | Col 1 (left aligned) | Col 2 (center aligned) | Col 3 (right aligned) |
  | :--- | :---: | ---: |
  | aa | ab | ac |
  | ba | bb | bc |
  | ca | cb | cc |

  The ["Markdown Table" extension by Takumi Ishii](https://marketplace.visualstudio.com/items?itemName=TakumiI.markdowntable) is very helpful to facilitate table editing and formatting in Markdown files. It also enables copying from an Excel spreadsheet and formatting the TSV content into a Markdown formatted table, among other features.

* Use Markdown to link an image (or any other files):

  ```Markdown
  ![image alt text (displays when image fails to load)](/path/to/image.png)
  ```

* It is highly recommended to use a modern text editor, such as the [Visual Studio Code (VS Code)](https://code.visualstudio.com/), to facilitate markdown editing.
  * For example, in VS Code, you can drag a picture (or any other file) into the markdown file while holding the `Shift` key to insert the formatted text.
  * There are also many -- probably too many -- choices of extensions for markdown. I have been using "Markdown All in One," "Markdown PDF," "markdownlint," "Selection Word Count," "Markdown Table," "Rainbow CSV," and "Excel Viewer."

### 2. Use Git and GitHub for version control and cloud backup

If you are new to Git, I highly recommend [the Software Carpentry Lesson for Git](https://swcarpentry.github.io/git-novice/index.html). Specifically, you can:

* Learn basic concepts of Git [here](https://swcarpentry.github.io/git-novice/01-basics.html).

* Install Git.
  * If you are using a new Mac, you probably have a quite new version of Git installed. Check by typing `git --version` in your terminal. If the version number is close to [the current version](https://git-scm.com/downloads), you can just use the pre-installed version.
  * Otherwise, follow instructions [here](https://carpentries.github.io/workshop-template/#git) to install Git on Windows, Mac or Linux systems.

* [Set up Git](https://swcarpentry.github.io/git-novice/02-setup.html) on your computer. Briefly:
  * Set your user name: `git config --global user.name "Your Name"`
  * Set your email (it's recommended to use a no-reply email, such as those provided by GitHub): `git config --global user.email "ID+username@users.noreply.github.com"`
  * Set line endings:
    * On Mac and Linux: `git config --global core.autocrlf input`
    * On Windows: `git config --global core.autocrlf true`
  * Set your text editor (assuming you use VS code): `git config --global core.editor "code --wait"`
  * Set default new branch name to be main: `git config --global init.defaultBranch main`
  * In addition to the general settings mentioned, you should also make sure file mode (e.g., whether it's executable) is ignored, since this can cause headaches when your git repo is on a shared drive. Run the following in your terminal: `git config --global core.fileMode false`

* [Use GitHub](https://swcarpentry.github.io/git-novice/07-github.html) for cloud backup.
  * It is recommended to use [SSH connections](https://docs.github.com/en/authentication/connecting-to-github-with-ssh).

* If you are using VS Code, you could easily commit and sync changes within the VS Code interface. If it keeps asking for the SSH passphrase, you can open a terminal window (inside VS code) and run `ssh-add`, which will ask for the SSH passphrase once and VS Code should no longer ask for it.
