# **Fundamentals of Bioinformatics 2026**
##
## **Course Objectives**
### By the end of this course, students will be able to:
- Navigate and Retrieve Data: Effectively query and retrieve nucleotide sequence data from major repositories like NCBI and ENA using both web interfaces and bash scripts.
- Analyze Sequence Similarity: Understand and apply heuristic search tools (BLAST) and interpret E-values, bit scores, and alignments.
- Perform Sequence Alignments: Execute pairwise and multiple sequence alignments (MSA) using algorithms like Clustal Omega to identify conserved regions.
- Design Molecular Tools: Apply thermodynamic principles to design and computationally validate PCR primers and DNA probes for laboratory use.
- Reconstruct Evolutionary History: Construct, evaluate, and aesthetically visualize phylogenetic trees using distance-based and character-based methods.
- Linux Command Line and Bash Script: Utilize Linux Command Line and Bash Script within Google Colab to explore and edit the sequence in FASTA format.
##

## **Reference and Lectures/Scripts**
### [Microbial Genome & Microbiome Analysis Course](https://github.com/UeenHuynh/MGMA_2024)
##
## [Course Overview](Lecture_00/Lecture_00_overview_2026May23.pdf)
##

## **Module 1: Review Molecular Biology, PCR and Sequencing Techniques**
### **Lecture 1: Central Dogma and DNA/RNA/Protein in Molecular Biology [Loi - 23/05/2026]**
- [PPT with Quizzes](Lecture_01/Lecture_01_The_Central_Dogma_Review.pdf)
- [Youtube record](https://youtu.be/IgNab0XOWpw)
### **Lecture 2: PCR and Applications [Loi - 26-27/05/2026]**
- Lecture, Quizzes and Homework: [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/drive/1FdqGKeCNgGJ2qnB-8UJpV-eJWH-lVZr0?usp=sharing)
- [Youtube record](https://youtu.be/raJz5Bjp9C8)
- Basic commands (echo, =, tr, printf, seq, '$()' and '$')
### **Lecture 3: Transcription and Translation; First Generation Sequencing (Sanger Sequencing), Next-Generation Sequecning (NGS) and Third-Generation Sequecning (TGS) [Loi - 30/05/2026]**
- Homework Review
- Transcription and Translation with exercises: [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/drive/1aJveHizBjoPWVNxYxrBFlZcoBuHHzeQ6?usp=sharing)
- Basic commands (User Defined Function, fold, sed -e 's/AUG/M/' and '${X:2}')
- [Lecture](Lecture_03/Lecture_03_Introduction_to_NGS.pdf)
- [YOUTUBE: Xét nghiệm gen hay xem bói 4.0](https://www.youtube.com/watch?v=Qac1Bd8V8_I)
- awk: Examples and Homework [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/drive/1h3-Jgspi2quJprcRFhm7fXXeFLi2WydX?usp=sharing)
##
## **Module 2: The Linux Environment & Data Retrieval**
### **Lecture 4: Introduction to Linux and Google Colab [Dan - 24/05/2026]**
- Theory: The importance of the command line in modern biotechnology and high-throughput data analysis. The file system hierarchy.
- Practice:
  + Setting up Google Colab for Bash using the %%bash magic cell. Basic commands (pwd, ls, cd, mkdir, mv, touch, cp, echo, cut, paste, grep, >, >>, wget, sort, |, cat, head, tail, wc).
  + Homwwork  [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/drive/1am6SY7Ihn6TAbq7z9DuGovAOX69rJwo9)
+ [Linux Commandline CheatSheet](https://www.digitalocean.com/community/tutorials/linux-commands)
### **Lecture 5: Parsing Biological Text Files [Dan - 31/05/2026]**
- [Theory:](/Lecture_05/NCBI%20Database.pdf)
  + Introduction to Nucleotide and Genome Database at NCBI
  + Standard biological data formats (FASTA, FASTQ, GenBank).
  + The concept of standard input, output, and piping.
- Practice: Using cat, head, tail, wc, and grep. Counting sequences in a multi-FASTA file using grep -c. [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/drive/1edgfVQXnEOqZc4E6LUVO8MrnUXRxlC2t?usp=sharing)
- Quiz: Recognizing FASTA format structures and correctly using pipes (|).
- Homework: Download a multi-FASTA file via a provided link using wget. Use grep and wc to report the total number of sequences and extract only the header lines into a new file.
### **Lecture 6: Programmatic Database Access with EDirect [Dan/Phuc - 02/06/2026]**
- [Theory:](Lecture_06/Lecture_06_Programmatic_Database_Access_with_EDirect.pdf) Programmatic Database Access with EDirect
- Practice (Colab): Installing EDirect in Colab. Using esearch -db nucleotide -query "term" | efetch -format fasta to download specific genes. [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/drive/1j2ZTk4NtOYawfG0uCcd018BRpLdiDnyQ?usp=sharing)
- Quiz: Constructing boolean search queries for NCBI and EDirect tool functions.
- Homework: Write a one-line bash command to search for the human BRCA1 mRNA sequence and download it directly into a file named brca1_human.fasta.
##
## **Module 3: Sequence Alignment and BLAST+**
### **Lecture 7: Principles of Sequence Alignment** [Loi - 07/06/2026]
- **Theory:** Homology, identity, and similarity. Global (Needleman-Wunsch) vs. Local (Smith-Waterman) alignment. Scoring matrices and gap penalties.
- **Practice (Colab):**
  + awk with Examples and Homework [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/drive/1h3-Jgspi2quJprcRFhm7fXXeFLi2WydX?)
  + Advanced text processing with `awk` to calculate GC content from a FASTA sequence downloaded in the previous lecture. 
- **Quiz:** Global vs. local alignment use cases; how gap penalties affect alignment scores.
- **Homework:** Write a short bash script utilizing `awk` that reads a sequence file and prints the total number of 'A', 'T', 'G', and 'C' nucleotides.

### **Lecture 8: Installing and Configuring Local BLAST+** [Dan/Loi - 06/06/2026]
- [**Theory**](Lecture_08/Basic_Local_Alignment.pdf) How the BLAST algorithm works heuristically. Understanding the differences between `blastn`, `blastp`, and `blastx`.
- **Practice (Colab):**
  + Using `apt-get install ncbi-blast+`. Creating a custom local BLAST database using `makeblastdb`.
  + [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/drive/1vumPUmW52kyz8qG5Z5TdyAku3ZsxuGc9?usp=sharing)
- **Quiz:**
  + Steps to format a FASTA file into a BLAST-searchable database.
  + [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/drive/1vumPUmW52kyz8qG5Z5TdyAku3ZsxuGc9?usp=sharing)
- **Homework:**
  + Download a bacterial genome (FASTA) via `wget`. Use `makeblastdb` to format it as a nucleotide database.
  + [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/drive/1vumPUmW52kyz8qG5Z5TdyAku3ZsxuGc9?usp=sharing)

### **Lecture 9: Executing and Parsing BLAST Searches** [Loi - 09/06/2026]
- **Theory:**
  + Understanding E-values, bit scores, and alignment outputs.
  + [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/drive/12PMqEAm0QK9epmGwMvIIsZIWh9IjFG53?usp=sharing)
- **Practice (Colab):**
  + [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/drive/12PMqEAm0QK9epmGwMvIIsZIWh9IjFG53?usp=sharing)
  + Running `blastn`. Customizing output formats using `-outfmt "6 qseqid sseqid pident evalue"`. Parsing tabular output using `awk` to filter for high-confidence hits.
- **Quiz:** Interpreting E-values and understanding the columns in BLAST tabular output format 6.
- **Homework:**
  + Query a mystery sequence against the custom bacterial database from Lecture 5. Output the results in tabular format and use `awk` to extract only hits with >95% identity.
  + [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/drive/12PMqEAm0QK9epmGwMvIIsZIWh9IjFG53?usp=sharing)
##

### **Module 4: Multiple Sequence Alignment (MSA)**
### **Lecture 10: MSA Algorithms** [Loi - 13/06/2026]
- **Theory:** [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/drive/1DjHBxA4uR781xqwzjcDoj_EjzGMYBSAI?usp=sharing)
     + Progressive alignment methods.
     + Why MSA is crucial for identifying conserved domains and evolutionary relationships.
- **Practice (Colab):**[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/drive/1DjHBxA4uR781xqwzjcDoj_EjzGMYBSAI?usp=sharing)
     + Installing Clustal Omega via `apt-get install clustalo`.
     + Preparing unaligned multi-FASTA files for input.
- **Quiz:** Progressive alignment pitfalls and the biological significance of conserved columns.
- **Homework:** [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/drive/1DjHBxA4uR781xqwzjcDoj_EjzGMYBSAI?usp=sharing)
     + Use EDirect to download 5 homologous sequences of the same gene across different species.
     + Combine them into a single file using `cat`.

### **Lecture 11: Running Clustal Omega via CLI** [Dan/Phuc - 14/06/2026]
- [**Theory:**](Lecture_11/Interpret_clustal_omega.pdf) Guide trees and hidden Markov models (HMMs) in alignment tools.
- **Practice (Colab):** Running `clustalo -i input.fasta -o output.aln --outfmt=clustal`. Reviewing the alignment using `cat` and `less`.
- **Quiz:** Command line flags for Clustal Omega and interpreting Clustal format (* vs . vs : symbols).
- **Homework:** Run Clustal Omega on the multi-FASTA file generated in Lecture 7. Output the file in both Clustal and FASTA formats.

### **Lecture 12: Alignment Trimming and Processing** [Dan/Phuc - 16/06/2026]
- **Theory:** The impact of poor alignments on downstream analyses. Identifying reliable blocks.
- **Practice (Colab):** [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/drive/1UVZc9XEs-HhK3ylsD6TGW_y7QoMetdy5?usp=sharing)
Installing and using a command-line trimmer (like `trimal`) to remove poorly aligned regions and gaps.
- **Quiz:** Why and when alignment trimming is necessary.
- **Homework:** Take the alignment output from Lecture 8 and use `trimal` to remove columns with more than 30% gaps.
##

## **Module 5: Primer and Probe Design**
### **Lecture 13: Thermodynamics of PCR Design** [Loi - 20/06/2026]
- **Theory:**
  + PCR kinetics. Rules for designing optimal primers and TaqMan probes (length, melting temperature $T_m$, GC content, avoiding secondary structures).
  + [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/drive/1nXsMs_k_CN2IZ4hYF68p-gHEVblV3vdG?usp=sharing)
- **Practice (Colab):**
  + Using `awk` to write a basic $T_m$ calculator script (using the Wallace rule: T_m = 2(A+T) + 4(G+C)).
  + [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/drive/1nXsMs_k_CN2IZ4hYF68p-gHEVblV3vdG?usp=sharing)
- **Quiz:** Primer design constraints and calculating basic T_m.
- **Homework:**
  + Create a Bash script that takes a 20-base primer string as an argument and outputs its GC% and estimated T_m.
  + [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/drive/1nXsMs_k_CN2IZ4hYF68p-gHEVblV3vdG?usp=sharing)

### **Lecture 14: Automated Design with Primer3** [Loi - 21/06/2026]
- **Theory:**
  + Primer3 core algorithms. Specificity, off-target binding penalties, and multiplexing constraints.
  + [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/drive/1p1H-LsVve8SOcMpHHXBrGIRYq06lRF0E?usp=sharing)
- **Practice (Colab):**
  + Installing Primer3 (`apt-get install primer3`). Formatting the Boulder-IO input text file. Running Primer3 core from the command line.
  + [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/drive/1p1H-LsVve8SOcMpHHXBrGIRYq06lRF0E?usp=sharing)
- **Quiz:**
  + Understanding the Primer3 input/output key-value pair format.
  + [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/drive/1p1H-LsVve8SOcMpHHXBrGIRYq06lRF0E?usp=sharing)
- **Homework:**
  + Write a Primer3 input file for a target sequence to design an amplicon between 150-250bp. Run Primer3 and extract the top forward and reverse primer sequences using `grep`.
  + [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/drive/1p1H-LsVve8SOcMpHHXBrGIRYq06lRF0E?usp=sharing)

### **Lecture 15: In-Silico PCR Validation** [Loi - 23/06/2026]
- **Theory:**
  + Ensuring primers do not bind off-target. Utilizing bioinformatics to simulate PCR before lab work.
  + [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/drive/1kD5FUk7XnUbhMg4o7LVtn3xdOgKamzHj?usp=sharing)
- **Practice (Colab):**
  + Using `blastn` with specialized parameters (`-task blastn-short`) to map designed primers against a reference genome.
  + [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/drive/1kD5FUk7XnUbhMg4o7LVtn3xdOgKamzHj?usp=sharing)
- **Quiz:**
  + Why standard BLAST settings fail for short primer sequences.
  + [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/drive/1kD5FUk7XnUbhMg4o7LVtn3xdOgKamzHj?usp=sharing)
- **Homework:**
  + Run an in-silico BLAST search for the primers designed in Lecture 11 against the human genome database. Analyze the output to confirm they only amplify the intended target region.
  + [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/drive/1kD5FUk7XnUbhMg4o7LVtn3xdOgKamzHj?usp=sharing)
##

## **Module 6: Phylogenetics**
### **Lecture 16: Fundamentals of Phylogenetics** [Loi - 27/06/2026]
- **Theory:**
  + Anatomy of a tree (nodes, branches, clades).
  + Distance-matrix (Neighbour Joining Tree and UPGMA) vs. Character-based (Maximum Parsimony and Maximum Likelihood) methods.
  + [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/drive/1Wk4w3-90yy6Nsslnalx-dmPu57K4ILDC?usp=sharing)
- **Practice (Colab):**
  + Introduction to the Newick tree format. Reading and understanding Newick strings using the command line.
  + [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/drive/1Wk4w3-90yy6Nsslnalx-dmPu57K4ILDC?usp=sharing)
- **Quiz:**
  + Differentiating between evolutionary models and reading Newick format.
  + [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/drive/1Wk4w3-90yy6Nsslnalx-dmPu57K4ILDC?usp=sharing)
- **Homework:**
  + Manually draw the tree represented by a provided Newick string: `((Human:0.1,Chimp:0.2):0.3,Mouse:0.5);.
  + [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/drive/1Wk4w3-90yy6Nsslnalx-dmPu57K4ILDC?usp=sharing)

### **Lecture 17: Tree Construction via Command Line** [Dan - 28/06/2026]
- [**Theory:**](Lecture_17/UI_phylogenetic_tree.pdf) Bootstrapping and statistical confidence in clades.
- **Practice (Colab):**
  + Installing FastTree (`apt-get install fasttree`). Generating a Maximum Likelihood tree from an MSA file generated in Lecture 11.
  + [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/drive/13tnVF7fHhTk7_LMkvHvS_7Ez2qAUiwnB#scrollTo=m3SoYBJxYn7y)
- **Quiz:** Command line execution of FastTree and interpreting bootstrap values.
- **Homework:** Build a phylogenetic tree using FastTree from a provided alignment of viral sequences. Save the resulting Newick tree to a file.
##

## **Module 7: Automation & Capstone**
### **Lecture 18: Bash Scripting for Pipelines** [Dan/Phuc - 28/06/2026]
- [**Theory:**]() The philosophy of reproducible bioinformatics. Using variables, loops (`for`, `while`), and conditional statements (`if`) in Bash.
- **Practice (Colab):** Writing a loop to automate BLAST searches for 10 different sequence files sequentially.
- **Quiz:** Bash scripting syntax (variable assignment, loop structure).
- **Homework:** Write a Bash `for` loop that iterates over three FASTA files, counts the sequences in each, and appends the results to a log file.

### **Lecture 19: Capstone Project Lab** [Loi - 28/06/2026]
- **Theory:** System integration. Reviewing how individual tools chain together.
- **Practice (Colab):** Writing a single, executable shell script (`analyze_gene.sh`) that:
1. Downloads a gene family using EDirect.
2. Aligns them using Clustal Omega.
3. Builds a phylogenetic tree using FastTree.
- **Quiz:** Final comprehensive review of the command-line pipeline.
- **Homework (Final Submission):** Submit the fully functional `analyze_gene.sh` script, properly commented, along with the output files generated by running it in Google Colab.
##
### **Lecture 20: Pre-Test** [Loi - 29&30/06/2026]
- [Pre-Test 0: 50 Multiple-Choice Questions](https://notebooklm.google.com/notebook/4c05873c-56fa-4a58-a47a-7ef9c0691721/artifact/15647063-f80f-45cc-be0f-d79600247896?utm_source=nlm_web_share&utm_medium=google_oo&utm_campaign=art_share_1&utm_content=&utm_smc=nlm_web_share_google_oo_art_share_1_)
- [Pre-Test 1: Linux Commandline and Bash Script (Module 1.1)](https://docs.google.com/forms/d/e/1FAIpQLSdZvCm90EgE_aS75roEbEqXlmRNnbWxYYa_wQNmwQ1czhIknA/viewform)
- [Pre-Test 2: Linux Command Line and Bash Script (Module 1.2 & 2.1)](https://docs.google.com/forms/d/e/1FAIpQLSfM5-hgrgwTXivR018neoZsXixMsD6QLrrMB8Cwr4ArssXZTQ/viewform)
- [Pre-Test 3: The Basic Molecular Biology and FASTA Format (Module 2.2 & 3.1)](https://docs.google.com/forms/d/e/1FAIpQLSfcU5acC2lbmEOVkXbk_j2vOjHTOdvn7YtSjQYbH0QtMWYCGA/viewform)
- [Pre-Test 4: Data Retrieval with NCBI EDirect (Module 3.2 & 4.1)](https://docs.google.com/forms/d/e/1FAIpQLSf68x7u6GigEfee6erMBa0m3Zfuzh9MiH4ik1iKNFS2tXBDdQ/viewform)
- [Pre-Test 6: PCR and Primer Design (Module 4.2 & 5.1)](https://docs.google.com/forms/d/e/1FAIpQLSfOW5NkhTpzKVEpFAnVE-OlMWzhfdAVjYWQ1GsNkq4v1qy-ZQ/viewform)
- [Pre-Test 7: Multiple Sequence Alignment (MSA) and Clustal Omega (Module 5.2)](https://docs.google.com/forms/d/e/1FAIpQLSdfk7ImdKiOKWZ9Q4TleltRyeuYnWd80p5WSmyT8jPHa8IkmQ/viewform)
- [Pre-Test 8: BLAST and Phylogenetic Analysis (Module 5.3 & Module 6)](https://docs.google.com/forms/d/e/1FAIpQLSdfk7ImdKiOKWZ9Q4TleltRyeuYnWd80p5WSmyT8jPHa8IkmQ/viewform)

##
## **Final Exam: Multiple Choice** [Uni - ??/??/2026]


