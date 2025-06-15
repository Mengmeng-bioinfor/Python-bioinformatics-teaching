# Week3

Hopefully you have already opened this document as a Jupyter Notebook and not simply as a pdf. If not, then you need to download the file *Week_3_Lab.ipynb* to an appropriate folder, and open the file.

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


# https://www.w3schools.com/python/python_lists.asp

# https://www.w3schools.com/python/python_tuples.asp

## Task 1 List

Given DNA sequence
dna_sequence = "AGCTTAGCTAGCTAGCTAGCTAGCTAGCTAGCT"

### 1. Calculate the length of the DNA sequence using a list-related function.

### 2. Count the number of 'C' and 'G' nucleotides in the DNA sequence using list-related functions.

### 3. Create a list of all unique nucleotides present in the DNA sequence using list-related functions.

### 4. Calculate the reverse complement of the DNA sequence using list-related functions.

Reversing and complementing a DNA sequence involves two distinct steps:

Reversing: This is simply taking a DNA sequence and reversing the order of its nucleotides. For example, if you have the sequence "ATCG", reversing it would give "GCTA".

Complementing: DNA is composed of four nucleotide bases: Adenine (A), Thymine (T), Cytosine (C), and Guanine (G). In the DNA double helix, Adenine always pairs with Thymine, and Cytosine always pairs with Guanine. Complementing a sequence means replacing each nucleotide with its pairing partner. So, for the sequence "ATCG", the complement would be "TAGC".

Together, reversing and complementing a sequence is often referred to as finding the "reverse complement". For the sequence "ATCG", the reverse complement would be "CGAT".

Importance:

Biology of the Double Helix: DNA exists as a double helix, with one strand running in the 5' to 3' direction and the other running in the 3' to 5' direction. When we talk about a specific DNA sequence in molecular biology, we often refer to the sequence of the 5' to 3' strand. But in various contexts, especially in laboratory experiments and certain analyses, the sequence of the complementary 3' to 5' strand becomes important. Knowing the reverse complement is crucial in these situations.

Primer Design in PCR: The polymerase chain reaction (PCR) is a fundamental molecular biology technique used to amplify DNA. To initiate the PCR, short DNA sequences known as primers are required. Often, one needs to design a primer that matches the reverse complement of a sequence of interest.

Genome Annotation and Analysis: During the process of annotating a genome or analyzing DNA sequences, it's essential to examine both the given DNA strand and its reverse complement to ensure all possible genes (which can be present on either strand) are identified.

DNA Replication: During DNA replication, the enzyme DNA polymerase synthesizes the new strand in the 5' to 3' direction. This means that while one strand (known as the leading strand) is synthesized continuously, the other (the lagging strand) is synthesized in fragments. Understanding the reverse complement sequence is crucial to understanding this process.

Explore the online tools by youself
https://arep.med.harvard.edu/labgc/adnan/projects/Utilities/revcomp.html

### 5. Find the starting index of the first occurrence of the subsequence 'AGCT' using list-related functions.


#### You might need: what is index()

The index() method is used to find the index or position of the first occurrence of a specified element within a list, tuple, or string. It returns the index of the first occurrence of the element in the sequence. If the element is not found, it raises a ValueError exception.

#### sequence.index(element[, start[, end]])

### 6. Split the DNA sequence into a list of codons (3-letter sequences) using list-related functions.


A for statement in Python is used for iteration or looping. It allows you to iterate over a sequence (such as a string, list, tuple, dictionary, or range) and perform a set of operations for each item in that sequence. The basic syntax of a for statement is as follows:

## Task 2 Tuple

Given protein sequence
protein_sequence = "MKEKLEEALDKIAEEKVYAKLENTAAGADFIKKTVEKESVDSKASLGGSGGELLEVGTVAKVEAGLNAEEAGNTKGAGEEGVAEEAKKEEGVEEK"

### 1. Create a tuple containing the amino acid residues found in the protein sequence.

### 2. Find the length of the protein sequence using a tuple-related function.

#### You might need: what is index()

The index() method is used to find the index or position of the first occurrence of a specified element within a list, tuple, or string. It returns the index of the first occurrence of the element in the sequence. If the element is not found, it raises a ValueError exception.

#### sequence.index(element[, start[, end]])

### 3. Calculate the frequency of each amino acid in the protein sequence using a tuple-related function.

#### You might need: what is import

It seems like you want to import a Python module or library. In Python, you can import modules or libraries to access their functions, classes, or variables. To import a module, you typically use the import keyword followed by the name of the module you want to import.

You can also use the import statement to import specific functions or variables from a module:

#### You might need: what is counter()

The Counter method in Python is part of the collections module and is used for counting the occurrences of elements in a collection, such as a list, tuple, string, or even another dictionary. It returns a dictionary-like object with elements as keys and their counts as values. This can be particularly useful in bioinformatics and various other data analysis tasks. Here's how you can use the Counter method:

### 4. Determine the position of the first occurrence of the amino acid 'E' using a tuple-related function.

#### You might need: 

In Python, indexing is the process of accessing individual elements or characters within a data structure like a string, list, or tuple. Python uses zero-based indexing, which means that the first element is at index 0, the second element is at index 1, and so on.

### 5. Create a tuple of the first 10 amino acids in the sequence.

# Advance exercise: Working with DNA Sequences

Given a list of DNA sequences, perform the following tasks:

##### Find the length of each sequence: 
Write a function that takes a list of DNA sequences (strings) and returns a list of tuples, where each tuple contains the DNA sequence and its length.

##### Identify sequences that start with a specific nucleotide: 
Write a function that filters the sequences starting with a given nucleotide (e.g., 'A') using list comprehensions and returns a list of tuples with the sequence and its length.

##### Find the GC content of each sequence: 
Write a function that calculates the GC content (percentage of 'G' and 'C' nucleotides) of each sequence and returns a list of tuples with the sequence, its length, and its GC content.

##### Filter sequences by length: 
Write a function that filters sequences by a given length threshold, returning only sequences longer than that threshold.

dna_sequences = [
    "ATGCGTACG",
    "CGTATGCGC",
    "ATGATGCGTACG",
    "GCGTAC",
    "AATGCG",
]

### Tasks:

#### 1. Find the length of each sequence.
Write a function sequence_lengths that takes the list of DNA sequences and returns a list of tuples (sequence, length).

#### 2. Filter sequences starting with a specific nucleotide.
Write a function filter_by_start that returns a list of sequences that start with a given nucleotide.

#### 3. Calculate the GC content.
Write a function gc_content that returns a list of tuples containing the sequence, its length, and its GC content as a percentage.

#### 4. Filter sequences by length.
Write a function filter_by_length that returns sequences longer than a specified length.

#### Expected Output:

Sequence lengths: [('ATGCGTACG', 9), ('CGTATGCGC', 9), ('ATGATGCGTACG', 12), ('GCGTAC', 6), ('AATGCG', 6)]

Sequences starting with 'A': [('ATGCGTACG', 9), ('ATGATGCGTACG', 12), ('AATGCG', 6)]

GC content: [('ATGCGTACG', 9, 55.55555555555556), ('CGTATGCGC', 9, 66.66666666666666), ('ATGATGCGTACG', 12, 50.0), ('GCGTAC', 6, 66.66666666666666), ('AATGCG', 6, 50.0)]

Sequences longer than 6: [('ATGCGTACG', 9), ('CGTATGCGC', 9), ('ATGATGCGTACG', 12)]
