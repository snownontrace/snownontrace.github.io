---
layout: protocols
title: repp-assisted plasmid design
author: Shaohe Wang
author_url: https://shaohewanglab.org
date: 2023-04-01
---

`repp` stands for repository-based plasmid design. It is a command line tool that is very useful to automate some steps in plasmid design. See [Timmons, J.J. & Densmore D. Repository-based plasmid design. PLOS One.](https://journals.plos.org/plosone/article?id=10.1371/journal.pone.0223935). Because `repp` is currently only available as a command line tool, the instructions below assumes some familiarity with the command line interface. Otherwise, please see [this page](https://swcarpentry.github.io/shell-novice/). We assume Windows users use the Git Bash program for their command line interface.

The original `repp` needs a multi-FASTA format sequence to build a database and the output is in json format, which is not convenient for typical molecular cloning work flow. [Cristian Goina](https://www.janelia.org/people/cristian-goina) from the Janelia Scientific Computing Software team has helped us to implement several important i/o features to adapt for our typical cloning work flow, including building a database from a directory of plasmid seuqences in FASTA or GenBank format, re-using existing primers, and outputting convenient csv format spreadsheets.

### 1. (Optional) Install and set up Git

Git is a powerful tool for version control. You don't need Git for installing and using `repp`, but I encourage you to learn about it if unfamiliar. I highly recommend [the Software Carpentry Lesson for Git](https://swcarpentry.github.io/git-novice).

* Learn basic concepts of Git [here](https://swcarpentry.github.io/git-novice/01-basics.html).

* Install Git.

  * If you are using a new Mac, you probably have a quite new version of Git installed. Check by typing `git --version` in your terminal. If the version number is close to [the current version](https://git-scm.com/downloads), you can just use the pre-installed version.
  * Otherwise, follow instructions [here](https://carpentries.github.io/workshop-template/#git) to install Git on Windows, Mac or Linux systems.

* [Set up Git](https://swcarpentry.github.io/git-novice/02-setup.html) on your computer.

### 2. Install the Janelia SciComp version of repp

`repp` has 3 dependencies: `go`, `primer3` and `blast`, which need to be installed first.
  
* Install `go` (version >= 1.19) following instructions [here](https://go.dev/doc/install).

* Install `blast`:

  * Go to [the NCBI website](https://blast.ncbi.nlm.nih.gov/Blast.cgi?PAGE_TYPE=BlastDocs&DOC_TYPE=Download) to download the BLAST+ software.
    * From this website, follow this [ftp download link](https://ftp.ncbi.nlm.nih.gov/blast/executables/blast+/LATEST/).
  * For __Mac__ (M1 or M2 chip OK), download "ncbi-blast-2.13.0+.dmg" for installation.
    * (Optional but good practice) Check the md5 sum of the downloaded installation package by `cd` into the download folder and run `md5 ncbi-blast-2.13.0+.dmg`. Make sure the md5 sum matches the ncbi-blast-2.13.0+.dmg.md5 in the ftp download list.
    * Open the dmg file to install blast.
    * Mac will warn you about this file is from "unidentified developer" and cannot be opened. You will need to go to "Security and Privacy" settings and click "Open Anyway" to open this installer.
    * Check whether installation is OK by running `which blastn`, which should print out the path to the `blastn` program (e.g., /usr/local/ncbi/blast/bin/blastn).
  * For __Windows__, download "ncbi-blast-2.13.0+-win64.exe"
    * (Optional but good practice) Check the md5 sum of the downloaded installation package by `cd` into the download folder and run `md5sum ncbi-blast-2.13.0+-win64.exe` in Git Bash. Make sure the md5 sum matches what is listed in ncbi-blast-2.13.0+-win64.exe.md5 in the ftp download list.
    * Open the exe file to install blast.
    * Check whether installation is OK by running `blastn -h` in Git Bash, which should print out the help message of the blastn program.

* Install `primer3`.

  * If you use Git, run `git clone https://github.com/primer3-org/primer3.git`.
  * If you don't use Git, go to [the Primer3 GitHub page](https://github.com/primer3-org/primer3), click on the green button `Code` and `Download ZIP`. Unzip it.
  * For __Mac__:
    * Assuming the source code of `primer3` is in the Downloads folder, run the following to compile, test, and install `primer3`:

      ```bash
      cd ~/Downloads/primer3/src
      make
      make test
      sudo make install
      ```

    * Check whether installation is OK by running `which primer3_core`, which should print out the path to the `primer3_core` program (e.g. /usr/local/bin/primer3_core).

  * For __Windows__:
    * Download and install [TDM-GCC MinGW Compiler](https://sourceforge.net/projects/tdm-gcc/).
    * Assuming the source code of `primer3` is in the Downloads folder, run the following to compile and test `primer3`:

      ```bash
      cd ~/Downloads/primer3/src
      mingw32-make TESTOPTS=--windows
      ```

    * Copy the "primer3/src" folder that contains the compiled binaries to your preferred location, e.g., "C:\Program Files\primer3\src".
    * Add the above folder to your `Path` Environment Variable.
      * Open Start Menu then type `Advanced system settings` and press Enter.
      * Click `Environment Variables`.
      * Select `Path` in the variable list and click `Edit...` to add the above directory.

* Install the Janelia SciComp version of `repp`.

  * If you use Git, run `git clone https://github.com/JaneliaSciComp/repp.git`.
  * If you don't use Git, go to [the Janelia SciComp GitHub page](https://github.com/JaneliaSciComp/repp), click on the green button `Code` and `Download ZIP`. Unzip it.
  * Assuming the source code of `repp` is in the Downloads folder, run the following to compile `repp`:

    ```bash
    cd ~/Downloads/repp/cmd/repp
    go build
    ```
  
  * The above generates an executable in the same folder.
    * For __Mac__, run `sudo mv repp /usr/local/bin/.` to move the executable to the `/usr/local/bin` folder. Type your password to give permission when prompted.
    * For __Windows__, copy the "repp.exe" file to your preferred location, e.g., "C:\Program Files\repp". Add this folder to your `Path` Environment Variable.
      * Open Start Menu then type `Advanced system settings` and press Enter.
      * Click `Environment Variables` towards the bottom of the dialogue.
      * Select `Path` in the variable list and click `Edit...` to add the above directory.

  * Check whether installation is OK by running `which repp`, which should print out the path to the `repp` program (e.g. /usr/local/bin/repp).

### 3. Use repp in your plasmid design work flow

* Download [repp_test.zip](assets/repp_test.zip) for testing.

* Add sequence databases using existing plasmids from repositories (e.g., Addgene, iGEM, DNASU) and local collections.

  For repository sequence collections, the original `repp` author has assembled FASTA files that are available from their S3 bucket. Run the following command to download and add them to the `repp` sequence database on your computer:

  ```bash
  # download repository FASTA files
  for db in igem addgene dnasu; do
    curl -o "$db.fa.gz" "https://repp.s3.amazonaws.com/$db.fa.gz"
    gzip -d "$db.fa.gz"
  done

  # add sequence DBs with the cost of ordering a plasmid from each source
  repp add database --name igem --cost 0.0 < igem.fa
  repp add database --name addgene --cost 85.0 < addgene.fa
  repp add database --name dnasu --cost 99.0 < dnasu.fa
  ```

  For local collections, put all sequence files (GenBank or FASTA format) in a directory. In the repp_test example, this directory is called "lab-plasmid-collection". Run the following command to add them:

  ```bash
  # -n is shorthand to --name
  # -c is shorthand for --cost
  # use "repp add database --help" to see more options
  repp add database -n lab -c 0.0 lab-plasmid-collection
  ```

  Note that adding sequence database is a one-time operation that stores the database files in a hidden directory (On Mac, they are in "~/.repp/dbs").

* It is optional to have a primer database, but it is good practice to have an organized local collection for re-using primers. In the repp_test example, the primer database is called "primer_database.csv", which has two columns, "primer_id" and "sequence":

  | primer_id | sequence                         |
  | :-------- | :------------------------------- |
  | oS1       | ACTTTTCGGGGAAATGTGCG             |
  | oS2       | GTGAGCAAAAGGCCAGCAAA             |
  | oS3       | GTGCCAGTGGTCTCTTGTTG             |
  | oS4       | GTGCCACCTGACGTCGACGGATCGGGAGATCT |
  | oS5       | GCCGGGTCCGCCATGGTGGCAGCGCTCTAG   |
  | oS6       | GGCATGGACGAGCTGTACAA             |
  | oS7       | TTCAAGTCTGTTCACACGCC             |
  | oS8       | CTTGCAGCAGATTCAGACCC             |
  | oS9       | CCACGTGGGCTTTATCTTCC             |

* Similarly, if you want to re-use synthesized fragments from your lab collection, you could provide a csv file with your existing synthesized fragments. In the repp_test example, the fragment database is called "frag_database.csv", which has two columns, "frag_id" and "sequence":

  | frag_id | sequence                         |
  | :------ | :------------------------------- |
  | f1      | TGGTGGTGGAGGCA...CTGTACAAGT      |

* Put together the target plasmid sequence with desired features in GenBank format. In the repp_test example, the target plasmid is called "pW256.gb".

  We use [ApE (A plasmid Editor)](https://jorgensen.biology.utah.edu/wayned/ape/) to edit and annotate DNA sequences. ApE is a free software written by M. Wayne Davis from University of Utah. You can use whatever software you prefer, but make sure to save it in GenBank format. Note that the default .ape file uses GenBank format and is compatible with `repp`.

* Run the `repp make sequence` command.

  The simpliest command is `repp make sequence -i pW256.gb`, which will use all available databases (in this case, "igem,addgene,dnasu,lab").

  To specify the database (e.g., only use local collection "lab"), use `repp make sequence -i pW256.gb -d lab`.

  To also specify the primer database and a fragment database, use `repp make sequence -i pW256.gb -d lab -m primer_database.csv -s frag_database.csv`. This result in two csv files: "pW256.output-strategy.csv" and "pW256.output-reagents.csv". The "pW256.output-strategy.csv" looks like this:

  | # 2023/04/02 11:37:01 |                  |            |          |      |           |
  | :-------------------- | :--------------- | :--------- | :------- | :--- | :-------- |
  | # Solution 1          |                  |            |          |      |           |
  | # Fragments:4         | Cost: 161.800000 |            |          |      |           |
  | Frag ID               | Fwd Primer       | Rev Primer | Template | Size | Match Pct |
  | pW256_1_pcr           | oS4              | oS5        | pW222    | 2911 | 100       |
  | pW256_2_pcr           | oS10             | oS11       | pR92     | 2888 | 100       |
  | syn1                  | N/A              | N/A        | N/A      | 743  | N/A       |
  | pW256_4_pcr           | oS12             | oS13       | pW222    | 4948 | 100       |

  The "pW256.output-reagents.csv" looks like this:

  | # Solution 1 |                                            |
  | :----------- | :----------------------------------------- |
  | Reagent ID   | Seq                                        |
  | *oS4         | GTGCCACCTGACGTCGACGGATCGGGAGATCT           |
  | *oS5         | GCCGGGTCCGCCATGGTGGCAGCGCTCTAG             |
  | oS10         | CGCTGCCACCATGGCGGACCCGGCGGAG               |
  | oS11         | GACTGCTTGCCTCCACCAC                        |
  | oS12         | GCATGGACGAGCTGTACAAG                       |
  | oS13         | CCGATCCGTCGACGTCAGGTGGCACTTTTCG            |
  | *syn1        | TGGTGGTGG...(long sequence)...AGCTGTACAAGT |

  The table in "pW256.output-strategy.csv" can be directly printed out for benchwork, while the reagent list in "pW256.output-reagents.csv" can be copied directly into the vendors for ordering primers (e.g., IDT) or synthetic fragments (e.g., Twist). Sometimes more than one solution is given, where the solution with the lowest may have more fragments than the solution with fewer fragments.

  Note that the primers found in primer_database.csv and the fragments found in frag_database.csv are marked with an asterisk, while new primers are numbered by incrementing from the last entry in the primer database spreadsheet. New primers can also be copied into primer_database.csv for future usage.
