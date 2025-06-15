Week 8
Hopefully you have already opened this document as a Jupyter Notebook and not simply as a pdf. If not, then you need to download the file to an appropriate folder, and open the file.

To open the file, if you have already installed Anaconda Individual Edition, then open Anaconda.Navigator, from which you can launch Jupyter Notebook.

(If working in the School of Computing labs, start Anaconda3 / Anaconda Prompt, then enter the following command specifying the path to the folder containing the file, and then open the file from the browser.)

The Jupyter Notebook App is a tool for creating documents (notebooks) containing both live code and text, as well as visualizations, etc. Various programming languages can be used, but here the focus will be on Python.

For more general resources:

Jupyter Notebook - https://jupyter.org/ Anaconda - https://www.anaconda.com/ Python - https://www.python.org/ The rest of this notebook is intended as an introduction to key features of Python and Jupyter Notebooks, irrespective of whether you have used Python before or not. It is not intended to be exhaustive, but will cover material that will be relevant in this module. In addition to this material, you are strongly encouarged to develop your knowledge of Python further through the use of other resources such as

The Python tutorial - https://docs.python.org/3/tutorial/ Both Python and Jupyter Notebooks are used in various areas, including data science, so it would be well worth your while to develop your skills in this area as much as possible.

Getting started One thing you should do at the outset is to save this noteback as a new notebook, so that you can change it as much as you want, but still go back to the original file if necessary. Go to File / Make a Copy. This creates a new notebook called Week_1_Lab-Copy1 in a file with the same name. You can change the name of the notebook (and the file) by going to File / Rename and changing it to Week_1_Lab_my_version for example, or by editing the name of the notebook at the top of the page beside the Jupyter symbol (just above the menu).

Cell Types We need to distinguish between different types of cells. This cell is a Markdown cell, whereas the next cell below is a Code cell. Markdown cells are for formatting text rather than for running code. To see how to format headings, use italics and bold font, for example, you can go into edit mode by double-clicking on a cell. Try it for this cell. To execute the cell (and so produce the formatted text), you can go to Cell / Run Cells or use the shortcut Ctrl-Enter. (You can find other keyboard shortcuts under the Help menu.) Markdown is very useful for mathematical notation such as 2⎯⎯√ . For further details on Markdown see Markdown in Jupyter Notebook.

The next cell below is a Code cell. You can also edit and run it as described above, but now it will execute the code and present the output below the cell.

# Task 1

Practice Problem: Python Function with if, for, and while

Write a function called process_numbers that takes a list of numbers as input and performs the following steps:


If the list is empty, return the string: "The list is empty".

Use a for loop to iterate through the list:

    If a number is even, add it to a new list called even_numbers.
    If a number is odd, add it to a new list called odd_numbers.
    If the number 0 appears in the list, print "Zero found in the list".

Use a while loop to calculate the sum of numbers in even_numbers.

Return a dictionary with:

    even_numbers: the list of even numbers.
    odd_numbers: the list of odd numbers.
    even_sum: the sum of the even numbers.

#Test
numbers = [10, 15, 20, 0, 3, 8, 7]
result = process_numbers(numbers)
print(result)

## Task 2

#### Objective: Write a Python function to analyze DNA sequences for specific characteristics.

##### Problem:
You are tasked with creating a Python program that:

    Checks whether a DNA sequence is valid (contains only A, T, C, and G).
    Counts the occurrences of each nucleotide in the sequence.
    Finds the complementary sequence using a loop.
    Stops processing when a stop codon (TAA, TAG, or TGA) is detected.


## Task 3

Problem: DNA Sequence Analysis
Write a Python script that includes the following functionality:

    1. A function called validate_dna(sequence) that checks if a given string is a valid DNA sequence. A valid DNA sequence contains only the characters A, T, C, and G. If invalid, the function should return False.

    2. A function called gc_content(sequence) that calculates the GC content (percentage of G and C bases) in a given DNA sequence.

    3. A function called find_motif(sequence, motif) that uses a for loop to find all start positions of a given motif (substring) in the DNA sequence.

    4. A function called reverse_complement(sequence) that calculates the reverse complement of a DNA sequence using a while loop.

#Test
dna_sequence = "ATGCGTACGTAGCTAGCT"
motif = "CGT"

if validate_dna(dna_sequence):
    print(f"GC Content: {gc_content(dna_sequence):.2f}%")
    print(f"Motif '{motif}' found at positions: {find_motif(dna_sequence, motif)}")
    print(f"Reverse Complement: {reverse_complement(dna_sequence)}")
else:
    print("Invalid DNA sequence!")


## Advance task

The following Python code is intended to calculate the GC content of a given DNA sequence. However, it contains several bugs. Your task is to debug the code and ensure it works correctly.

