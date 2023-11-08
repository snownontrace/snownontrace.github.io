---
layout: protocols
title: repp-assisted plasmid design
author: Shaohe Wang
author_url: https://shaohewanglab.org
date: 2023-11-08
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

* Install 3 dependencies: `go`, `primer3`, and `blast`. Skip to the next step if you are updating `repp`.

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
      * (Optional) Assuming the source code of `primer3` is in the Downloads folder, run the following to compile and test `primer3`:

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
    * For __Mac__, run `sudo mv repp /usr/local/bin/.` to move the executable to `/usr/local/bin` or your preferred location. Type your password to give permission if prompted.
    * For __Windows__, copy the "repp.exe" file to your preferred location, e.g., "C:\Program Files\repp". Add this folder to your `Path` Environment Variable.
      * Open Start Menu then type `Advanced system settings` and press Enter.
      * Click `Environment Variables` towards the bottom of the dialogue.
      * Select `Path` in the variable list and click `Edit...` to add the above directory.

  * Check whether installation is OK by running `which repp`, which should print out the path to the `repp` program (e.g. /usr/local/bin/repp).

### 3. Use repp in your plasmid design work flow

* Download [repp_test.zip](assets/repp_test.zip) for testing.

* (Optional) Add sequence databases from remote repositories (e.g., Addgene, iGEM, DNASU).

  As direct synthesis of DNA fragments becomes more affordable, the advantage of PCR amplification from existing plasmids diminishes. Moreover, acquiring a plasmid from repositories introduces additional time costs. If you have access to basic plasmid backbones, you may omit this step.

  The original `repp` author has assembled FASTA files from Addgene, iGEM, and DNASU, and made it available from the S3 bucket. Run the following command to download and add them to the `repp` sequence database on your computer:

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

* Add sequence databases from local collections.

  Put all sequence files (GenBank or FASTA format) in a directory. In the repp_test example, this directory is called "lab-plasmid-collection". Run the following command to add them:

  ```bash
  # -n is shorthand for --name
  # -c is shorthand for --cost
  # run "repp add database --help" for more options
  repp add database -n lab -c 0 lab-plasmid-collection
  ```

  Note that adding sequence database is a one-time operation that stores the database files in a hidden directory. Adding a new directory to a database with the same name(e.g., -n lab) will overwrite it.

  * On Mac, they are in "~/.repp/dbs".
  * On Windows, they are in "C:/users/username/.repp/dbs".

* (Recommened) Organize your primer database.

  Although not strictly required, it is highly recommended to create an organized primer database for re-using primers. The primer database parameter "-m" of the Janelia version of repp accpets either a single spreadsheet or a folder containing multiple spreadsheets. When your primer database contains hundred or thousands of primers, it can be cumbersome to scroll down to the bottom of the spreadsheet to add new primers. Instead, it is much easier to maintain a small active spreadsheet with one or more archived spreadsheets. The primer database spreadsheet must have the "primer_id" and "sequence" columns, and optionally other columns for additional notes.

  In the repp_test example, the "primer_database" folder has two spreadsheets: "1_archived_primer.csv" and "2_active_primer.csv". This is how the "2_active_primer.csv" looks like:

  | primer_id | sequence                         |
  | :-------- | :------------------------------- |
  | oS41      | ACTTTTCGGGGAAATGTGCG             |
  | oS42      | GTGAGCAAAAGGCCAGCAAA             |
  | oS43      | GTGCCAGTGGTCTCTTGTTG             |
  | oS44      | CTATTACCATGGTGATGCGGTTTTGGCAGTAC |
  | oS45      | ACTGGATCTCTGCTGTCCCT             |
  | oS46      | GGCATGGACGAGCTGTACAA             |
  | oS47      | TTCAAGTCTGTTCACACGCC             |
  | oS48      | CTTGCAGCAGATTCAGACCC             |
  | oS49      | CCACGTGGGCTTTATCTTCC             |

* (Optional) Organize your fragment database.
  
  Following the same logic of re-using primers, you may also wish to re-use synthesized fragments. For this purpose, you can organize your synthesized fragment database similarly as the primer database. Similar to the primer database parameter, the synthesized fragment database parameter "-s" can also accpet a single spreadsheet or a folder containing multiple spreadsheets.

  In the repp_test example, the "fragment database" folder has two spreadsheets: "1_archived_frag.csv" and "2_active_frag.csv". This is how the "2_active_frag.csv" looks like:

  | frag_id | sequence                          |
  | :------ | :-------------------------------- |
  | syn4    | atgtca...(long sequence)...ataacc |
  | syn5    | CAGGGA...(long sequence)...TCAAAG |

* Put together the target plasmid sequence in GenBank format.

  In the repp_test example, the target plasmid is called "pW256.gb".

  We use [ApE (A plasmid Editor)](https://jorgensen.biology.utah.edu/wayned/ape/) to edit and annotate DNA sequences. ApE is a free software written by M. Wayne Davis from University of Utah. You can use whatever software you prefer, but make sure to save it in GenBank format. Note that the default .ape file uses GenBank format and is compatible with `repp`.

* Run the `repp make sequence` command.

  The simpliest command is `repp make sequence -i pW256.gb`, which uses all available databases (in this case, "igem,addgene,dnasu,lab") and default parameters.

  To specify the database (e.g., only use local collection "lab"), use `repp make sequence -i pW256.gb -d lab`.

  To also specify the primer database and a fragment database, use `repp make sequence -i pW256.gb -d lab -m primer_database -s frag_database`. This result in two csv files: "pW256.output-strategy.csv" and "pW256.output-reagents.csv".
  
  The first 5 columns of "pW256.output-strategy.csv" is shown below. Other columns (Match Pct, GC%, 50 low GC%, 50 high GC%, and Homopolymer) can help users decide whether certain fragments may be difficult to PCR or to synthesize.

  | # 2023/11/08 13:37:36  |                           |            |          |      |
  | :--------------------- | :------------------------ | :--------- | :------- | :--- |
  | # Solution 1           |                           |            |          |      |
  | # Fragments:5 (3 - pcr | 2 - synth)                |            |          |      |
  | # Cost: 179.510000     | Adjusted Cost: 179.510000 |            |          |      |
  | Frag ID                | Fwd Primer                | Rev Primer | Template | Size |
  | pW256_1_pcr            | oS44                      | oS45       | pW212    | 1983 |
  | syn5                   | N/A                       | N/A        | N/A      | 350  |
  | pW256_3_pcr            | oS50                      | oS51       | pR92     | 2876 |
  | syn6                   | N/A                       | N/A        | N/A      | 766  |
  | pW256_5_pcr            | oS52                      | oS53       | pW212    | 5555 |

  The "pW256.output-reagents.csv" is shown below. The priming region and Tm columns can help users optimize PCR amplification conditions.

  | # Solution 1 |                                     |                         |       |       |
  | :----------- | :---------------------------------- | :---------------------- | :---- | :---- |
  | Reagent ID   | Seq                                 | Priming Region          | Tm    | Notes |
  | *oS44        | CTATTACCATGGTGATGCGGTTTTGGCAGTAC    | TGATGCGGTTTTGGCAGTAC    | 59.12 |       |
  | *oS45        | ACTGGATCTCTGCTGTCCCT                | ACTGGATCTCTGCTGTCCCT    | 59.96 |       |
  | oS50         | GCGGAGTGCAACATCAAAGT                | GCGGAGTGCAACATCAAAGT    | 59.41 |       |
  | oS51         | GACTGCTTGCCTCCACCAC                 | GACTGCTTGCCTCCACCAC     | 60.97 |       |
  | oS52         | ACGCGTTAAGTCGACAATCA                | ACGCGTTAAGTCGACAATCA    | 57.95 |       |
  | oS53         | CAAAACCGCATCACCATGGTAATAGCGATGACTAA | ACCATGGTAATAGCGATGACTAA | 57.2  |       |
  | *syn5        | CAGGGA...(long sequence)...CAAAGTG  | N/A                     | N/A   |       |
  | syn6         | TGGTGG...(long sequence)...CAATCAA  | N/A                     | N/A   |       |
  
  Note that pre-existing primers and synthesized fragments are marked with an asterisk. The IDs of new primers and synthesized fragments are incremented from the last entry of the last spreadsheet of the database.

  Sometimes `repp` generates multiple solutions, because some solution may have a larger cost but fewer fragments. You can choose your favorite solution to move forward.

* Order reagents (primers and synthesized fragments).

  For new primers, you can copy the first two columns from the "*output-reagents.csv" file into the active primer database spreadsheet, and order them from your favorite vendor. We routinely order primers from IDT.

  Similarly, for new fragments that need to be synthesized, you can copy the first two columns into the active spreadsheet of the synthesized fragments database, and order them from your favorite DNA fragment vendor. We use Twist for its unparalleled low cost (9 cents per bp).

* PCR amplification and Gibson Assembly.

  Print the table in "*output-strategy.csv" for bench work reference.
  
  Follow [this protocol](https://snownontrace.github.io/PCR-amplification.html) for PCR amplification using a high-fidelity DNA polymerase.

  Follow [this protocol](https://snownontrace.github.io/gibson-assembly.html) for assembling the fragments using Gibson Assembly.
