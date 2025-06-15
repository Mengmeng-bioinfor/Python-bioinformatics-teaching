# Week 9

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

This task involves working with a Python script designed to analyze genomic data. The script includes some common bioinformatics operations like reading FASTA files, performing sequence alignments, and calculating some basic statistics. Your task will be to debug this script and add appropriate comments.

Your task is to:

1. Debug the script: Ensure that it runs smoothly with a sample FASTA file. You might need to handle exceptions or edge cases that are not currently addressed.
2. Add comments: Improve the script by adding detailed comments that explain what each part of the code does, especially in complex or critical sections.
3. Optimize the code: If you find any inefficient parts of the code, try to optimize them for better performance, especially if dealing with large genomic datasets.

# Task 2 

Scenario: Debugging a Python Script for ORF Analysis in a DNA Sequence

#### Task Overview:
1. Goal: Identify all potential open reading frames (ORFs) in a given DNA sequence.
2. Input: A string representing a DNA sequence.
3. Process: The script should scan the sequence, look for start and stop codons, and identify all ORFs.

#### Comments and Debugging Strategy:

##### Functionality: The find_orfs function scans the DNA sequence for start codons and then looks for the nearest stop codon to identify an ORF.

##### Debugging: A break statement was added to exit the loop once a stop codon is found. This prevents the identification of overlapping ORFs that share the same start codon.

##### Testing: The script is tested with a sample DNA sequence. Adjustments or more sophisticated tests might be required for different or longer sequences.

# Task 3

Task Description
You are provided with a Python script that aims to find common motifs (subsequences) across a set of DNA sequences. The script attempts to identify these motifs using a naive approach and then calculates their frequency in each sequence.

#### Debugging and Comments
The script seems straightforward, but there are a few areas we can improve or debug:

1. Motif Counting Logic: The current logic counts each occurrence of a motif across all sequences. If we want to count how many sequences contain a motif at least once, this logic needs to be adjusted.
2. Input Validation: We should add validation for the input sequences and motif length.
3. Optimization: While the naive approach works for short sequences, it might be inefficient for longer sequences. However, since the data file isn't provided, we'll keep the approach as is.
