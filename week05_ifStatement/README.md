# Week 5

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

## Task 1

For a given list of DNA sequences, and you want to filter and process them based on their length and composition. You have the following requirements:

#### 1.Filter sequences that are longer than 100 base pairs.
#### 2.Check if a sequence contains a specific motif, such as "AGTC."
#### 3.Classify sequences as either coding or non-coding based on whether they contain a start codon ("ATG").

#Sample DNA sequences
dna_sequences = [
    "ATGCGTACGTACGTACTGACTAGCTAGCTA",    # Coding sequence with start codon
    "ACGTACGTACGTACGTACGTACGTACGTACGT",  # Non-coding sequence
    "ACTGACGTAGCTACGTAACGTAGCTAGCTG",    # Non-coding sequence
    "ATGGCTAGCTAGCTAGCTAGCTAGCTA",       # Coding sequence with start codon
]

sequence= dna_sequences[0]

length= len(sequence)

print(length)

## Task 2 

Assume there is a list of tuples, where each tuple represents information about a gene, such as its name, expression level, and mutation status.

#### Complete to filter and process this data using nested if statements according to the following pseudocode.

1. We initialize two empty lists, high_expression_genes and mutated_genes, to store the results of our analysis.

2. We loop through each gene's tuple in gene_data.

3. Inside the loop, we first check if the gene has a high expression level (expression level > 20). If it does, we add it to the high_expression_genes list.

4. If the gene has a high expression level and is also mutated (mutation_status is "Mutation"), we print a message to indicate it's a high-expression mutated gene.

5. We then check if the gene is mutated (mutation_status is "Mutation"), and if it is, we add it to the mutated_genes list.

6. Finally, we display the lists of high-expression genes and mutated genes.

#Sample gene data as tuples: (name, expression_level, mutation_status)
gene_data = [
    ("GeneA", 10, "Mutation"),
    ("GeneB", 25, "Normal"),
    ("GeneC", 5, "Mutation"),
    ("GeneD", 15, "Normal"),
]

## Task 3 

#### Filter a set of DNA sequences based on specific criteria. 

In this example, there is a set of DNA sequences stored in a dictionary. Please use nested if statements to filter the sequences based on two criteria: 
#### high GC content and length. 
The sequences that meet both criteria are considered valid sequences.

You can work with your specific bioinformatics criteria. 

Advanced applications of nested if statements in bioinformatics often involve more complex conditions and additional data processing steps, such as sequence alignment, motif detection, or phylogenetic analysis.

#Define a set of DNA sequences
dna_sequences = {
    "sequence1": "ATGAGCTAGCTAGCTAGCTGAGCTAGCTAG",
    "sequence2": "ATGAGCTAGCTAGCTAGCTGAGCTAGCTAG",
    "sequence3": "ATGACGCTAGCTAGCTAGCTGAGCTAGCTAG",
    "sequence4": "ATGAGCTAGCTAGCTAGCTGAGCTAGCTAG",
}

#Define threshold values
gc_content_threshold = 0.6
sequence_length_threshold = 30

## Task 4 

Use a nested if statement to determine the type of DNA sequence based on the counts of nucleotides A, T, C, and G. 

Counts the occurrences of each nucleotide and then uses nested if statements to classify the sequence as purine-rich, pyrimidine-rich, or mixed based on the most abundant nucleotides. 

#### Pseudocode:
1. Create a DNA sequence as a string.
2. Initialize a dictionary to store nucleotide counts (A, T, C, G).
3. Initialize variables to count each nucleotide.
4. Iterate through the DNA sequence:
   - For each character in the sequence:
     - If it is 'A', increment the 'A' count.
     - If it is 'T', increment the 'T' count.
     - If it is 'C', increment the 'C' count.
     - If it is 'G', increment the 'G' count.
5. Determine the type of DNA sequence:
   - If 'A' and 'T' are the most abundant nucleotides, it's likely a purine-rich sequence.
   - If 'C' and 'G' are the most abundant nucleotides, it's likely a pyrimidine-rich sequence.
   - If there's a balanced distribution, it's a mixed sequence.
6. Print the type of DNA sequence.

#Create a DNA sequence
dna_sequence = "ATCGAGTACCGTAAAG"

## Advance task 

#### Case Study: 
Identifying a DNA Motif in Sequences

#### Scenario:
You are a bioinformatics researcher working with DNA sequences. You want to find and count the occurrences of a specific DNA motif within a list of DNA sequences. Motifs are represented as tuples of DNA bases.

1. We have a list of DNA sequences, and we represent the motif we're searching for as a tuple.
2. We use a dictionary to store the indices of sequences where the motif is found and the respective counts.
3. We use nested if statements to check if the current three bases in the sequence match the motif.
4. If the motif is found, we increment the count, and if the count is greater than 0, we record the sequence index and count in the dictionary.
5. Finally, we display the results by iterating through the dictionary.

#### Pseudocode:

1. Define a list of DNA sequences
2. Define the motif to search for as a tuple
3. Initialize an empty dictionary to store sequence indices and motif counts

4. Loop through each sequence in the list:
    a. Initialize a count for the current sequence
    b. Loop through the sequence using a range(len(sequence) - 2):
        i. If the current three bases match the motif:
            - Increment the count
    c. If the count is greater than 0:
        i. Store the sequence index and count in the dictionary

5. Display the results: Iterate through the dictionary and print the sequence index and count.

#List of DNA sequences
dna_sequences = [
    "AGTACAGTGGTAGTACAGTCTAGTACAGT",
    "TAGTACAGTCTAGTACAGTGGTAGTACAG",
    "CTAGTACAGTGGTAGTACAGTGGTAGTAC",
    "TGGTAGTACAGTGGTAGTACAGTCTAGTA"
]


## Case: DNA Sequence-Based Species Classification

In this case, we have a simple dataset of DNA sequences. Each sequence consists of four nucleotide bases: A, T, C, and G. Based on the characteristics of the sequence (such as which bases are present and their distribution), we want to classify the species as either Species A or Species B.

## Task: Algorithm implementation

### Use if statement to write an algorithm based on decision tree

### This algorithm can:

### Based on the given features: the types of bases contained and their proportions, predict which species the base fragment belongs to.

We will make classification decisions based on the following rules:

#### If the sequence starts with an "A," it is more likely to be Species A.

#### If the sequence contains more than one "T," it may also be classified as Species A.

#### Otherwise, it is likely Species B.

### Decision tree

A decision tree is a type of machine learning algorithm used for both classification and regression tasks. It is a tree-like structure that models decisions and their possible outcomes. The decision tree algorithm splits the data into subsets based on the value of certain features (or attributes) in a step-by-step process, leading to a decision or prediction at the end.

#### How a Decision Tree Works:

##### Splitting the Data:

The tree begins at the root node and splits the data into subsets based on the value of the most important feature. The algorithm determines which feature to use by calculating the best possible split (using measures like information gain, Gini impurity, or variance reduction).

##### Recursive Partitioning:

After the first split, the algorithm continues to split each subset recursively. For each subset, it chooses another feature and splits the data further.

The goal is to make each subset as homogeneous as possible—meaning, each subset should ideally contain only data points from a single class (or with similar values for regression).

##### Stopping Criteria:

##### The splitting process continues until the tree reaches a stopping criterion. 

A maximum depth for the tree (to prevent overfitting).

A minimum number of data points required in a node.

No more significant information gain from splitting further.

Once a stopping criterion is met, the node becomes a leaf and the algorithm assigns a class label (in classification) or a value (in regression) to that node.

#DNA sequences and their corresponding species
data = [
    {'sequence': 'ATCG', 'species': 'A'},
    {'sequence': 'ACGT', 'species': 'B'},
    {'sequence': 'ATTT', 'species': 'A'},
    {'sequence': 'CGGT', 'species': 'B'}
]


