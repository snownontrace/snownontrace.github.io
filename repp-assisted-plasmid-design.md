---
layout: protocols
title: repp-assisted plasmid design
author: Shaohe Wang
author_url: https://shaohewanglab.org
date: 2023-04-01
---

`repp` is a command line tool that helps automate some steps in plasmid design. See [Timmons, J.J. & Densmore D. Repository-based plasmid design. PLOS One.](https://journals.plos.org/plosone/article?id=10.1371/journal.pone.0223935). [Cristian Goina](https://www.janelia.org/people/cristian-goina) from the Janelia Scientific Computing Software team has helped us to implement several important features to adapt this tool for our everyday molecular cloning work flow.

We mainly use it to generate a cloning strategy table and a reagent list (primers and synthetic DNA fragments) after we put together the sequence of a target plasmid. For example, after installation and importing existing plasmids from the lab as a database ("lab"), we can run a one-line command like this:

```bash
repp make sequence -i pS1.gb --dbs lab -m ./primer_database.csv
```

The above command will generate two csv files, "pS1.output-strategy.csv" and "pS1.output-reagents.csv":

| # 2023/04/01 15:40:16 |                  |            |                  |      |           |
| :-------------------- | :--------------- | :--------- | :--------------- | :--- | :-------- |
| # Solution 1          |                  |            |                  |      |           |
| # Fragments:4         | Cost: 139.570000 |            |                  |      |           |
| Frag ID               | Fwd Primer       | Rev Primer | Template         | Size | Match Pct |
| pS1_1_pcr             | oS25             | oS26       | pW219_lenti_pEF1 | 873  | 100       |
| pS1_2_syn             | N/A              | N/A        | N/A              | 514  | N/A       |
| pS1_3_pcr             | oS27             | oS2        | pW84_pSpCas9_BB_ | 2728 | 100       |
| pS1_4_syn             | N/A              | N/A        | N/A              | 601  | N/A       |

| # Solution 1 |                                       |
| :----------- | :------------------------------------ |
| Reagent ID   | Seq                                   |
| *oS2         | GTGAGCAAAAGGCCAGCAAA                  |
| oS25         | ACTGGCTTTCCATTCGACCC                  |
| oS26         | GGAAATCTCGAGCGTCGACA                  |
| oS27         | CCCTAGTGATGGAGTTGGCC                  |
| pS1_2_syn    | CTGTCG...(long sequence)...GGCCA      |
| pS1_4_syn    | TTTTGCTG...(long sequence)...TCGACCCC |

The table in "pS1.output-strategy.csv" can be directly printed out for benchwork, while the reagent list in "pS1.output-reagents.csv" can be copied directly into the vendors for ordering primers (e.g., IDT) or synthetic fragments (e.g., Twist).

Because `repp` is currently only available as a command line tool, the instructions below assumes that you are facimilar with command line interface or unix shell. See [this page](https://swcarpentry.github.io/shell-novice/setup.html) to set up shell on your specific system.

### 1. (Optional) Install and set up Git

You don't need Git for installing and using `repp`, but it is a powerful tool for version control and I encourage you to learn it if you are unfamiliar with it. I highly recommend [the Software Carpentry Lesson for Git](https://swcarpentry.github.io/git-novice/index.html). Specifically, you can:

* Learn basic concepts of Git [here](https://swcarpentry.github.io/git-novice/01-basics/index.html).

* Install Git.
  * If you are using a new Mac, you probably have a quite new version of Git installed. Check by typing `git --version` in your terminal. If the version number is close to [the current version](https://git-scm.com/downloads), you can just use the pre-installed version.
  * Otherwise, follow instructions [here](https://carpentries.github.io/workshop-template/#git) to install Git on Windows, Mac or Linux systems.

* [Set up Git](https://swcarpentry.github.io/git-novice/02-setup/index.html) on your computer.

### 2. Install repp

`repp` has 3 dependencies: `go`, `primer3` and `blast`, which need to be installed first.
  
* Install `go` (version >= 1.19) following instructions [here](https://go.dev/doc/install).

* Install `blast`:

  * Go to [the NCBI website](https://blast.ncbi.nlm.nih.gov/Blast.cgi?PAGE_TYPE=BlastDocs&DOC_TYPE=Download) to download the BLAST+ software.
    * From this website, follow this [ftp download link](https://ftp.ncbi.nlm.nih.gov/blast/executables/blast+/LATEST/).
  * If you are using a Mac with M1 or M2 chip, download the "ncbi-blast-2.13.0+.dmg" file.
    * (Optional but good practice) Check the md5 sum of the downloaded installation package by `cd` into the download folder and run `md5 ncbi-blast-2.13.0+.dmg`.
    * Check if the md5 matches the ncbi-blast-2.13.0+.dmg.md5 in the ftp download list.
  * Open the dmg file to install blast.
    * Mac will warn you about this file is from "unidentified developer" and cannot be opened. You will need to go to "Security and Privacy" settings and click "Open Anyway" to open this installer.
  * Check whether installation is OK by running `which blastn`, which should print out the path to the `blastn` program (e.g., /usr/local/ncbi/blast/bin/blastn).

* Install `primer3`.

  * If you use Git, run `git clone https://github.com/primer3-org/primer3.git`.
  * If you don't use Git, go to [the Primer3 GitHub page](https://github.com/primer3-org/primer3), click on the green button `Code` and `Download ZIP`. Unzip it.
  * Assuming the source code of `primer3` is in the Downloads folder, run the following to install `primer3`:

    ```bash
    cd ~/Downloads/primer3/src
    make
    make test
    sudo make install
    ```

  * Check whether installation is OK by running `which primer3_core`, which should print out the path to the `primer3_core` program (e.g. /usr/local/bin/primer3_core).

* Install `repp`.

  * If you use Git, run `git clone https://github.com/JaneliaSciComp/repp.git`.
  * If you don't use Git, go to [the Janelia SciComp GitHub page](https://github.com/JaneliaSciComp/repp), click on the green button `Code` and `Download ZIP`. Unzip it.
  * Assuming the source code of `repp` is in the Downloads folder, run the following to install `repp`:

    ```bash
    cd ~/Downloads/repp/cmd/repp
    go build
    sudo mv repp /usr/local/bin/.
    ```

  * Check whether installation is OK by running `which repp`, which should print out the path to the `repp` program (e.g. /usr/local/bin/repp).

### 3. Using repp
