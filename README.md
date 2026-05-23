# Fundamentals of Bioinformatics 2026
##
## Course Objectives
### By the end of this course, students will be able to:
- Navigate and Retrieve Data: Effectively query and retrieve nucleotide sequence data from major repositories like NCBI and ENA using both web interfaces and R scripts.
- Analyze Sequence Similarity: Understand and apply heuristic search tools (BLAST) and interpret E-values, bit scores, and alignments.
- Perform Sequence Alignments: Execute pairwise and multiple sequence alignments (MSA) using algorithms like Clustal Omega to identify conserved regions.
- Design Molecular Tools: Apply thermodynamic principles to design and computationally validate PCR primers and DNA probes for laboratory use.
- Reconstruct Evolutionary History: Construct, evaluate, and aesthetically visualize phylogenetic trees using distance-based and character-based methods.
- Linux Command Line and Bash Script: Utilize Linux Command Line and Bash Script within Google Colab to explore and edit the sequence in FASTA format.
##
## Module 1: The Linux Environment & Data Retrieval
### Lecture 1: Introduction to Linux and Google Colab
- Theory: The importance of the command line in modern biotechnology and high-throughput data analysis. The file system hierarchy.
- Practice (Colab): Setting up Google Colab for Bash using the %%bash magic cell. Basic commands (pwd, ls, cd, mkdir, echo).
- Quiz: Linux file system navigation and basic command syntax.
- Homework: Create a specific directory structure using the command line and write a simple text file containing a short DNA sequence using echo and redirection (>).
### Lecture 2: Parsing Biological Text Files
- Theory: Standard biological data formats (FASTA, FASTQ, GenBank). The concept of standard input, output, and piping.
- Practice (Colab): Using cat, head, tail, wc, and grep. Counting sequences in a multi-FASTA file using grep -c.
- Quiz: Recognizing FASTA format structures and correctly using pipes (|).
- Homework: Download a multi-FASTA file via a provided link using wget. Use grep and wc to report the total number of sequences and extract only the header lines into a new file.
### Lecture 3: Programmatic Database Access with EDirect
- Theory: Introduction to NCBI Entrez Direct (EDirect). Translating web searches into command-line queries (esearch, efetch).
- Practice (Colab): Installing EDirect in Colab. Using esearch -db nucleotide -query "term" | efetch -format fasta to download specific genes.
- Quiz: Constructing boolean search queries for NCBI and EDirect tool functions.
- Homework: Write a one-line bash command to search for the human BRCA1 mRNA sequence and download it directly into a file named brca1_human.fasta.
