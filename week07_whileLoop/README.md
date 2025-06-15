# Week 7

Hopefully you have already opened this document as a Jupyter Notebook and not simply as a pdf. If not, then you need to download the file to an appropriate folder, and open the file.

To open the file, if you have already installed Anaconda Individual Edition, then open Anaconda.Navigator, from which you can launch Jupyter Notebook.

(If working in the School of Computing labs, start Anaconda3 / Anaconda Prompt, then enter the following command specifying the path to the folder containing the file, and then open the file from the browser.)

The Jupyter Notebook App is a tool for creating documents (notebooks) containing both live code and text, as well as visualizations, etc. Various programming languages can be used, but here the focus will be on Python.

For more general resources:

Jupyter Notebook - https://jupyter.org/
Anaconda - https://www.anaconda.com/
Python - https://www.python.org/
The rest of this notebook is intended as an introduction to key features of Python and Jupyter Notebooks, irrespective of whether you have used Python before or not. It is not intended to be exhaustive, but will cover material that will be relevant in this module. In addition to this material, you are strongly encouarged to develop your knowledge of Python further through the use of other resources such as

The Python tutorial - https://docs.python.org/3/tutorial/
Both Python and Jupyter Notebooks are used in various areas, including data science, so it would be well worth your while to develop your skills in this area as much as possible.

Getting started
One thing you should do at the outset is to save this noteback as a new notebook, so that you can change it as much as you want, but still go back to the original file if necessary. Go to File / Make a Copy. This creates a new notebook called Week_1_Lab-Copy1 in a file with the same name. You can change the name of the notebook (and the file) by going to File / Rename and changing it to Week_1_Lab_my_version for example, or by editing the name of the notebook at the top of the page beside the Jupyter symbol (just above the menu).

Cell Types
We need to distinguish between different types of cells. This cell is a Markdown cell, whereas the next cell below is a Code cell. Markdown cells are for formatting text rather than for running code. To see how to format headings, use italics and bold font, for example, you can go into edit mode by double-clicking on a cell. Try it for this cell. To execute the cell (and so produce the formatted text), you can go to Cell / Run Cells or use the shortcut Ctrl-Enter. (You can find other keyboard shortcuts under the Help menu.) Markdown is very useful for mathematical notation such as  2⎯⎯√
 . For further details on Markdown see Markdown in Jupyter Notebook.

The next cell below is a Code cell. You can also edit and run it as described above, but now it will execute the code and present the output below the cell.

# Task 1

Generates a random DNA sequence and calculates its GC content, which is the percentage of guanine (G) or cytosine (C) bases.

Once an acceptable sequence is found (with GC content above 50%), it stops and prints the final sequence. 

# Task 2

Parsing genetic sequence data.

1. Parse through a dictionary of gene sequences.
2. Calculate the GC content, which is the percentage of bases in a DNA sequence that are either guanine (G) or cytosine (C).
3. Search for a specific DNA motif within the sequence.
4. Create the reverse complement of the DNA sequence.
5. Use control structures (if, for, while) efficiently to accomplish the tasks.

#Define a dictionary with gene identifiers as keys and DNA sequences as values
gene_sequences = {
    'gene1': 'ATGCGTACGTAGCTAGCTGACTG',
    'gene2': 'GCGCTATGCTAGCATGCTAGCTG',
    'gene3': 'ATGCGCATATCGTACGATCG',
}

# Task 3 

Exercise: You're working with a dataset of genetic sequences where each sequence is represented by a string composed of four nucleotides (adenine (A), cytosine (C), guanine (G), and thymine (T)). You want to perform the following tasks:

1. Create a dictionary where each key is a unique genetic sequence (string) and its value is a tuple containing the count of each nucleotide in the sequence.
2. For each sequence, determine if it has a high GC content. GC content is considered high if it is greater than 60% of the sequence.
3. Create a set that contains only the sequences with high GC content.
4. Write a loop that iteratively reduces the sequences by removing one nucleotide from the end of each sequence until the length of each sequence is less than 10 or no sequences are left.

#Define a function to calculate GC content
def calculate_gc_content(sequence):
    gc_content = (sequence.count('G') + sequence.count('C')) / len(sequence)
    return gc_content > 0.6  # Returns True if GC content is higher than 60%

#Example list of genetic sequences
sequences = ['ATCGGCTA', 'GCGCGCGC', 'ATATATAT', 'CGCGATCGA']

# Task 4

Calculates the frequency of each nucleotide in a DNA sequence and identifies the most frequent nucleotide

# Define a DNA sequence (in practice, this would be read from a file)
dna_sequence = "AGCTTTTCATTCTGACTGCAACGGGCAATATGTCTCTGTGTGGATTAAAAAAAGAGTGTCTGATAGCAGC"

# Advance Task 5

## Exercise Description
Given a DNA sequence, perform the following:

#### 1. Transcribe the DNA sequence into RNA.

Ensure that only valid DNA nucleotides are transcribed.
   
   
#### 2. Translate the RNA sequence into a peptide chain.

Create a dictionary representing the codon table.
Use a for loop to iterate through the RNA sequence in codons (triplets) and map each to a peptide.
   
#### 3. Metabolize specific peptides in the sequence into metabolites.

If a specific peptide sequence is encountered, break it down into a set of metabolites.
Store the metabolites in a list, and ensure no duplicates by converting it to a set.

#Define the codon table as a dictionary mapping RNA codons to peptides
codon_table = {
    'AUG': 'Methionine', 'UGG': 'Tryptophan', 'UAC': 'Tyrosine', 'CGG': 'Arginine', # Example codons
    
    # ... (other codons should be filled in here for a complete table)
    
    # 'UAA', 'UAG', 'UGA' are stop codons and are not included in the codon table
    
}


