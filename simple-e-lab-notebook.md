---
layout: protocols
title: A simple electronic lab notebook using Markdown and Git
author: Shaohe Wang
author_url: https://shaohewanglab.org
date: 2022-09-17
---

The most commonly used elements in a lab notebook are text, tables and images, which can be easily organized in Markdown files. This can be greatly facilitated by a modern text editor, such as **Visual Studio Code**. The most important feature of an electronic lab notebook is to trace editing history, which can be conveniently achieved by **Git**.

### 1. Use Markdown to organize text, tables and images.

* Learn markdown basics [here](https://www.markdownguide.org/basic-syntax/).
* Practice markdown following [this tutorial](https://www.markdowntutorial.com/).
* Use Markdown to make a table:
```
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

* Use Markdown to link an image (or other files):
```
![image alt text (displays when image fails to load)](/path/to/image.png)
```
* Most modern text editors have excellent support for markdown editing.
  * A popular choice is [Visual Studio Code (VS Code)](https://code.visualstudio.com/).
  * I previously used [Atom](https://atom.io/), but it will be discontinued in December 2022. I then switched to VS Code.


### 2. Use Git and GitHub for version control and cloud backup.

If you are new to Git, I highly recommend [the Software Carpentry Lesson for Git](https://swcarpentry.github.io/git-novice/index.html). Specifically, you can:
* Learn basic concepts of Git [here](https://swcarpentry.github.io/git-novice/01-basics/index.html).
* [Install Git](https://carpentries.github.io/workshop-template/#git) on Windows, Mac or Linux systems.
* [Set up Git](https://swcarpentry.github.io/git-novice/02-setup/index.html) on your computer.
* [Using GitHub](https://swcarpentry.github.io/git-novice/07-github/index.html) for cloud backup.
  * It is recommended to use [SSH connections](https://docs.github.com/en/authentication/connecting-to-github-with-ssh).
