# Week 4

Hopefully you have already opened this document as a Jupyter Notebook and not simply as a pdf. If not, then you need to download the file *Week_4_Lab.ipynb* to an appropriate folder, and open the file.

To open the file, if you have already installed ***Anaconda Individual Edition***, then open *Anaconda.Navigator*, from which you can launch *Jupyter Notebook*.

(If working in the School of Computing labs, start *Anaconda3 / Anaconda Prompt*, then enter the following command specifying the path to the folder containing the file, and then open the file from the browser.)

The Jupyter Notebook App is a tool for creating documents (notebooks) containing both live code and text, as well as visualizations, etc. Various programming languages can be used, but here the focus will be on Python. 

For more general resources:

- Jupyter Notebook - https://jupyter.org/
- Anaconda - https://www.anaconda.com/
- Python - https://www.python.org/

The rest of this notebook is intended as an introduction to key features of Python and Jupyter Notebooks, irrespective of whether you have used Python before or not. It is not intended to be exhaustive, but will cover material that will be relevant in this module. In addition to this material, you are strongly encouarged to develop your knowledge of Python further through the use of other resources such as

- The Python tutorial - https://docs.python.org/3/tutorial/

Both Python and Jupyter Notebooks are used in various areas, including data science, so it would be well worth your while to develop your skills in this area as much as possible.

## Getting started

One thing you should do at the outset is to save this noteback as a new notebook, so that you can change it as much as you want, but still go back to the original file if necessary. Go to *File / Make a Copy*. This creates a new notebook called *Week_1_Lab-Copy1* in a file with the same name. You can change the name of the notebook (and the file) by going to *File / Rename* and changing it to *Week_1_Lab_my_version* for example, or by editing the name of the notebook at the top of the page beside the Jupyter symbol (just above the menu).

### Cell Types

We need to distinguish between different types of cells. This cell is a **Markdown cell**, whereas the next cell below is a **Code cell**. Markdown cells are for formatting text rather than for running code. To see how to format headings, use italics and bold font, for example, you can go into edit mode by double-clicking on a cell. Try it for this cell. To execute the cell (and so produce the formatted text), you can go to *Cell / Run Cells* or use the shortcut *Ctrl-Enter*. (You can find other keyboard shortcuts under the *Help* menu.) Markdown is very useful for mathematical notation such as $\sqrt{2}$. For further details on Markdown see <a href="https://www.datacamp.com/community/tutorials/markdown-in-jupyter-notebook" >Markdown in Jupyter Notebook</a>.

The next cell below is a Code cell. You can also edit and run it as described above, but now it will execute the code and present the output below the cell. 

## Task 3 Set

#### 1. Filtering Unique Sequences:

Given a list of DNA sequences, you can use sets to filter out unique sequences
sequences = ["ATGCA", "AGCTA", "ATGCA", "GCTAA", "AGCTA"]

#### 2.Finding Common Elements:

If you have two lists of genes, you can find the common genes between them using sets:

gene_list1 = {"GeneA", "GeneB", "GeneC", "GeneD"}

gene_list2 = {"GeneC", "GeneD", "GeneE", "GeneF"}

#### 3.Union of Protein Domains:

Suppose you have two sets of protein domains and you want to find the union of these sets:

domain_set1 = {"DomainA", "DomainB", "DomainC"}

domain_set2 = {"DomainB", "DomainD", "DomainE"}

#### 4.Differential Gene Expression:

You can use sets to identify genes that are differentially expressed between two conditions. For example, if you have two sets of genes representing condition A and condition B, you can find the genes unique to each condition:

genes_condition_A = {"GeneA", "GeneB", "GeneC", "GeneD"}

genes_condition_B = {"GeneC", "GeneD", "GeneE", "GeneF"}

#### 5.Set Operations on DNA Sequences:

You can perform set operations on DNA sequences, such as finding sequences that are unique to a particular sample:

sample1_sequences = {"ATGCA", "AGCTA", "TACGT"}

sample2_sequences = {"AGCTA", "GCTAA", "TTGCA"}

#### 6.Checking for Sequence Membership:

You can check if a particular sequence is present in a dataset using sets:

sequences = {"ATGCA", "AGCTA", "TACGT", "GCTAA"}

sequence_to_check = "AGCTA"

## Task 4 Dictionary

Bioinformatics often involves working with biological data, such as DNA or protein sequences, and performing various operations on them. Python dictionaries can be useful for storing and manipulating this type of data. Here's a simple bioinformatics practice example using Python dictionaries:

#### 1. Counting Nucleotide Frequencies in a DNA Sequence

Let's say you have a DNA sequence, and you want to count the frequency of each nucleotide (A, T, C, and G) in the sequence. You can use a Python dictionary to achieve this:

# DNA sequence
dna_sequence = "ATGCTAAAGCTATGCTAAATATGCTAAATGCTAAAAACAATGCTAAATGCTAATGCTAAAAAG"
#### 2. Counting Nucleotide Frequencies in a DNA Sequence

# Please use plaint language to write pseudocode for the following code.

GC content, also known as guanine-cytosine content, is a measure of the proportion of guanine (G) and cytosine (C) nucleotides in a DNA or RNA sequence. It is an essential parameter in bioinformatics and molecular biology because variations in GC content can have significant implications for the structure and function of DNA or RNA molecules.

GC content, or the ratio of guanine (G) and cytosine (C) nucleotides to the total number of nucleotides in a DNA or RNA sequence, is an important parameter in bioinformatics and molecular biology for several reasons:

1. **Species Identification**: GC content can vary significantly between different species. It can be used to help identify or differentiate between species. For example, the GC content in the genomes of some organisms can serve as a unique signature.

2. **Genome Analysis**: GC content can be a key factor in the analysis of entire genomes. It can help researchers understand the characteristics and evolution of a genome. Genomic islands, regions with significantly different GC content than the rest of the genome, can indicate the presence of horizontally transferred genes.

3. **Primer Design**: In polymerase chain reaction (PCR) and other molecular biology techniques, the GC content of primers is crucial. It affects primer binding and specificity. Primers with similar GC content are more likely to anneal correctly, improving the accuracy of molecular experiments.

4. **Melting Temperature (Tm) Calculation**: The GC content influences the melting temperature (Tm) of a DNA duplex. DNA strands with higher GC content have a higher Tm, which can be important in applications like PCR and hybridization studies.

5. **Stability of DNA/RNA Structures**: Higher GC content can lead to increased stability in DNA and RNA structures, such as secondary structures in RNA. Understanding these structures is essential in the study of RNA function and regulation.

6. **Gene Function and Regulation**: The GC content of coding regions and regulatory elements can provide insights into gene expression and regulation. It can be a factor in gene prediction and annotation.

7. **Phylogenetics**: GC content can be used in phylogenetic analysis. It can help researchers construct evolutionary trees and determine the relatedness of different species or organisms.

8. **Hybridization and Annealing**: In experiments like Southern blotting or in situ hybridization, the GC content of probes or targets is important for successful hybridization.

9. **GC Skew and Replication**: Analysis of GC skew (the difference between the G and C counts on the leading and lagging strands) is used to study DNA replication and gene orientation in genomes.

In summary, GC content is a valuable metric in bioinformatics and molecular biology that can provide insights into a variety of biological processes, genomic characteristics, and experimental design. It helps researchers make informed decisions in various applications, from primer design to understanding evolutionary relationships between species.

# DNA sequence
dna_sequence = "ATGCTAAAGCTATGCTAAATATGCTAAATGCTAAAAACAATGCTAAATGCTAATGCTAAAAAG"

#### Solution:

1. We create a sample DNA sequence represented as a string.
2. We initialize a dictionary called nucleotide_counts to store the counts of 3. each nucleotide (A, T, C, G). The initial counts are all set to 0.
4. We iterate through each character in the dna_sequence string using a for loop.
5. For each nucleotide in the sequence, we check if it's a valid nucleotide and update its count in the nucleotide_counts dictionary.
6. After counting all the nucleotides, we print the counts for each nucleotide.
7. We calculate and print the GC content by summing the counts of G and C and dividing it by the total sequence length.

#### 3. Counting Nucleotide Frequencies in a DNA Sequence

Bioinformatics often involves working with sequence data, and the FASTA format is commonly used to represent biological sequences, such as DNA or protein sequences. In this example, I'll show you how to work with FASTA sequences using Python dictionaries.

FASTA format typically consists of a header line starting with ">" followed by the sequence data. Multiple sequences can be stored in a single FASTA file. We'll create a dictionary where the headers are the keys, and the sequences are the values.

Here's a step-by-step practice of how to read and work with FASTA sequences(gene.fna) using Python dictionaries:

# Modify the following code to obtain Nucleotide counts results

#### Counting Nucleotide Frequencies in a DNA Sequence


# Please use plaint language to write pseudocode for the following code.

#Define a function to calculate the GC content of a DNA sequence.
def calculate_gc_content(sequence):
    # Count the occurrences of 'G' and 'C' in the sequence.
    gc_count = sequence.count('G') + sequence.count('C')
    
    # Get the total count, which is the length of the sequence.
    total_count = len(sequence)
    
    # Calculate the GC content as a percentage.
    gc_content = (gc_count / total_count) * 100
    
    # Return the calculated GC content.
    return gc_content

#Define a DNA sequence that you want to calculate the GC content for.
sequence = "ATGCATGCATGC"

#Call the calculate_gc_content function to compute the GC content.
gc_content = calculate_gc_content(sequence)

#Print the GC content with two decimal places as a percentage.
print(f'GC content: {gc_content:.2f}%')
