---
layout: protocols
title: Guide RNA Design
author: Madison Mehlferber
author_url: https://www.linkedin.com/in/madison-mehlferber-97127b146/
date: 2020-07-24
---

[Guide RNA Design](https://blog.addgene.org/how-to-design-your-grna-for-crispr-genome-editing) allows for the establishment of precise insertion or deletions relating to your gene of interest(GOI). Designing guide RNA's(gRNA) provides the foundation for powerful and efficient regulation and manipulation within your system of interest. 

<img src=" />

### 1. Identify your gene of interest(GOI). 

Identify the GOI that you are interested in regulating expression of. Find the correct nomenclature of this gene. This can be accomplished via a simple Google Search. 

### 2. Find your GOI and Sequence 

Use a genome browser specific to the species you will be working with. Often it's helpful to get the reference name from a source like [NCBI gene database](https://www.ncbi.nlm.nih.gov/gene/?term=Mus+musculus+Kif5b). Find the genetic sequence relevant to the gene information on the GOI. Good sources to accomplish this include: 
* [NCBI BLAST] (https://blast.ncbi.nlm.nih.gov/Blast.cgi?PROGRAM=blastn&PAGE_TYPE=BlastSearch&LINK_LOC=blasthome)  This BLAST site should come up when using the NCBI gene/protein database.

*[UCSC genome browser](https://genome.ucsc.edu/cgi-bin/hgGateway) to browse your species genome in relation to the GOI to get a concept of of your GOI relevant to size and different variants. 

*[Ensembl](https://useast.ensembl.org/index.html )

### 3. Go to NCBI Gene to find the protein sequence of your GOI under the "translation section" 

<img src="/images/translation.png" alt="translation NCBI gene viewer"/>


### 4. Perform a [BLAST search,](https://blast.ncbi.nlm.nih.gov/Blast.cgi) 

Use the BLAST (protein preferably) of your GOI and observe the degree of conservation that is present within your protein sequence. A high percentage of conservation means evolutionarily the entire sequence is important for functionality so it is important to create a guide RNA(gRNA) that would effectively knock out the majority of the mRNA. 


### 5. Pick your Genome Browser 

We recommend using [Ensembl](https://useast.ensembl.org/index.html) as it offers easy to download sequence information on your GOI that can be translated across multiple platforms however you can use whichever browse

### 6. Download the Gene Info File 
Using the [Ensembl browser](https://useast.ensembl.org/Mus_musculus/Gene/Summary?db=core;g=ENSMUSG00000006740;r=18:6201002-6242174) download the data on your gene in the genbank format by clicking on the "Export Data" button on the left of the page(highlighted in the image below). 

* when downloading leave the output as "Feature strand". Unclick "Deselect all" and click "Gene information" and modify "5' flanking sequence" and "3' Flanking Sequence" to 250bp. Save the output in the appropriate directory for your project. Ensembl offers 3 ways to save the files:  HTML, txt and .zip file. You can simply drag and drop the txt version of the download into a gene viewer such as [SnapGene Viewer](https://www.snapgene.com/snapgene-viewer/) or the free software [ApE](https://jorgensen.biology.utah.edu/wayned/ape/) 

### 7. Open the Downloaded Genetic info 

You can simply drag and drop the txt version of the download into a gene viewer such as [SnapGene Viewer](https://www.snapgene.com/snapgene-viewer/) or the free software [ApE](https://jorgensen.biology.utah.edu/wayned/ape/). 

### 8. Open the File

Open the downloaded .txt containing the genetic info into SnapGene Viewer to visuslize the location of the exons of the mRNA and select an exon within the first half of the mRNA. This small region will serve as the small 20 nucleotide long gRNA. If the region you pick for this is too far within the strand the protein/gene you're interested in manipulating could just be truncated rather than silenced. 


### 9. Paste this Region into [CRISPOR](http://crispor.tefor.net/)

Paste the small mRNA (the 20 nt sequence you chose) into the [CRISPOR](http://crispor.tefor.net/) website. And select the proper genome you're working with. 
<img src="/images/crispor.png alt="CRISPOR"/>

*insert your exon sequence copied from SnapGene viewer into the browser
*Select the genome to which you are working with (<em>mus musculus, Human, C.elegans</em> etc. 
*Pick the protospacer motif (PAM) specific to the Cas9 protein you will be using. (N stands for any nucleotide). 
*Click "Submit" to send the job 
<img src ="/images/crispor-data-load.png" alt="sumbitting the crispor job"/>

### 10. Interpreting Results

The browser will return a list of the best gRNA constructs with the least likelihood of off targeting. It's best to pick 3 of the top results meeting a criteria of the <em>highest score, efficiency, and least off target effects</em>/

<img src="/images/result.png" alt=Results"/>

### 11. Getting Results from CRISPOR 


You can then download the information returned into an excel file and prioritize and pick the gRNA's you will be using in your gRNA experiment. 

### 12. Once you've chosen gRNA's....

Remember its best to pick 3 in case some end up not being efficient. 

*Copy and paste the sequences into the provided spreadsheet which helps to orient you to the proper system to order you gRNA's. 
*the spreadsheet will aid in the process of: 
- naming the gRNA's
- establishing the complimentary strand and subtracting 3 nucleotides from the end of the sequence
- taking the complimentary strand and getting the reverse compliment
- adding a g to the reverse compliment 

Look to the [spreadsheet for further details](https://docs.google.com/spreadsheets/d/1wMQTqPC93D7E9Z52ceQLryW_jSJGQQyQGTDpyhQHAiM/edit#gid=0). This spreadsheet works under the assumption that you will be using a 96-well dish. 

1. Paste one of the gRNA sequences from the downloaded file from CRISPOR into the sheet keeping the format of "#guideID, targetSeq, mitSpecScore, offtargetCount, targetGenomeGeneLocus")
2. Drag the columns down for the entirety of the sequences you've entered. 
3. The calculations wil occur automatically. 
3. The grey section includes the work for specifying the gRNA segment and establishing the reverse compliment and getting the complimentary regions. 
4. Look to the section in purple under the title "This is what you need to order:". The purple region will include the results and provide the reverse region established from the grey region and the complimentary region with the needed "sticky ends" from the Esp31 cut (the enzyme that will be used). 

Your oligos are now ready to order to establish the gRNA's that will be involve in the gRNA design experiment!!


