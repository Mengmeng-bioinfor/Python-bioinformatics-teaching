# Week 6

Hopefully you have already opened this document as a Jupyter Notebook and not simply as a pdf. If not, then you need to download the file to an appropriate folder, and open the file.

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

## 
Task 1 

A common advanced task in bioinformatics that involves extensive use of for loops is analyzing biological sequence data, such as DNA, RNA, or protein sequences. Motifs are recurring, conserved sequences within a set of DNA, RNA, or protein sequences that are often indicative of biological function.

The steps you would follow:
1. Read multiple DNA sequences from a file.
2. Define a list of known transcription factor binding motifs.
3. Slide a window of fixed size across each DNA sequence.
4. For each position of the window, check if the sequence within the window matches any known motifs.
5. Count the occurrences of each motif across all sequences.
6. Output the frequencies of each motif.

#Define a list of DNA sequences
dna_sequences = [
    "ATCGTACGATCGATCGATCGCTAGACGTATCG",
    "CGATCGATCGATACGATCGATCGTACGATCGA",
    "TAGCTAGCATCGATCGATCGATCGTACGATC"
]

#Define a list of known motifs
motifs = ["ATCG", "CGAT", "GATC"]

## Task 2

Find all the possible open reading frames (ORFs) in a DNA sequence.

An ORF is a sequence of DNA that has the potential to be translated into protein. It starts with a start codon (ATG in DNA) and ends with a stop codon (TAA, TAG, or TGA in DNA). This task requires scanning the sequence in all three possible reading frames on both the forward and reverse strands, looking for start and stop codons, and extracting the sequences between them.

The task involves:

1. Taking a DNA sequence as input.
2. Generating the reverse complement of the DNA sequence to search both strands.
3. Scanning each reading frame for start and stop codons.
4. Extracting sequences between start and stop codons.
5. Handling overlapping ORFs, as they can start before the previous ORF ends.

#Test the function with a sample DNA sequence
sample_dna = "ATGGCCATGTAAATGCCCCCCGAGCGGGTAAATGTTTGAAATGAGCTAAATGGCCATGTAAATGCCCATGGCCATGTAAATGCCCCCCGAGCGGGTAAATGTTTGAAATGAGCTAACCCGAGCGGGTAAATGTTTGAAATGAGCTAA"

## Advance Task 3

1. Simulate gene expression data for 100 genes in a control group and a disease group, with 10 samples in each group.
2. Perform a t-test for each gene to compare the control and disease groups.
3. Collect genes that show a significant difference in expression (p-value < 0.05).
4. Use for loops to iterate over the genes and calculate the t-test.

#### SciPy is an open-source Python library used for scientific and technical computing. It is an essential tool in the field of bioinformatics, as well as in other domains that require complex mathematical computations, such as physics, engineering, and mathematics. 

#### Core Package in Scientific Computing: SciPy is built on top of NumPy, which provides support for array-like data structures and mathematical operations. SciPy extends this functionality with a collection of mathematical algorithms and convenience functions.

#### Modules: It is organized into subpackages covering different scientific computing domains. These are some of the key subpackages:

scipy.integrate: Provides several integration techniques including support for ordinary differential equations.
scipy.linalg: Contains all the functions in NumPy's numpy.linalg, plus some other more advanced ones not contained in NumPy.
scipy.optimize: Provides functions for the optimization of functions and root finding.
scipy.signal: Tools for signal processing.
scipy.sparse: Provides data structures for large, sparse matrices, along with associated algorithms.
scipy.stats: Contains a large number of probability distributions and statistical functions.
scipy.spatial: Provides functions to work with spatial data, including KD-trees, distance computations, and spatial transformations.
Usage in Bioinformatics: In bioinformatics, SciPy can be used for tasks like statistical analysis of gene expression data, modeling of biological processes, and simulations of biochemical kinetics, among others.

#### Interoperability: SciPy works well with other libraries, such as Pandas for data manipulation and Matplotlib for plotting. This interoperability makes it a versatile choice for a wide range of applications.

#Example of use of scipy

from scipy import stats

#Sample data representing gene expression levels for two different conditions
gene_expression_condition_1 = [2.1, 2.4, 2.3, 2.1, 2.2]
gene_expression_condition_2 = [2.8, 2.9, 3.1, 3.0, 2.9]

#Perform a t-test to determine if there is a significant difference between the two conditions
t_statistic, p_value = stats.ttest_ind(gene_expression_condition_1, gene_expression_condition_2)

print(f"T-statistic: {t_statistic}, P-value: {p_value}")

#Typically, a p-value less than 0.05 is considered statistically significant
if p_value < 0.05:
    print("The difference in gene expression between the two conditions is statistically significant.")
else:
    print("No significant difference in gene expression between the two conditions was found.")

# T- test and P value

The t-test is a statistical test that is used to compare the means of two groups and determine if they are statistically different from each other. It's particularly useful when dealing with small sample sizes and when the variance of two normal distributions is unknown and assumed to be equal.

Here's a breakdown of the t-test and the p-value:

### T-test:
#### Types of T-tests:

1. Independent samples t-test: Compares means for two groups.
2. Paired sample t-test: Compares means from the same group at different times.
3. One-sample t-test: Tests the mean of a single group against a known mean.

#### Assumptions:

1. Independence of observations: 
2. The data points in each group should be independent of each other.
3. Normality: The data in each group should be roughly normally distributed.
4. Variance: The variance between the two groups should be approximately equal (for an independent t-test).

#### Calculation:

The t-value is calculated by taking the difference between the two sample means and dividing it by the standard error of the difference. 
The standard error is derived from the standard deviations of the two samples and their respective sample sizes.

#### Interpretation:

A higher absolute value of the t-statistic indicates a greater difference between groups relative to the variability within the groups.

### P-value:
#### Definition:

The p-value is the probability of observing a test statistic as extreme as, or more extreme than, the observed value under the null hypothesis. In simpler terms, it measures how compatible your data is with the null hypothesis (often that there is no effect or no difference).

#### Threshold:

A commonly used threshold for significance is 0.05. If the p-value is less than 0.05, the result is declared statistically significant. This means that if there was no actual difference (the null hypothesis is true), there would be less than a 5% chance of observing a difference as large as the one in your sample due to random chance alone.

#### Interpretation:

A low p-value indicates that the observed data is unlikely under the null hypothesis. It suggests that the null hypothesis may not be a good fit for the data and that the alternative hypothesis (that there is an effect or a difference) might be true.
Conversely, a high p-value suggests that the observed data is likely under the null hypothesis, and there is no reason to reject the null hypothesis.

#Set the random seed for reproducibility
np.random.seed(0)

#Define the number of genes and samples
num_genes = 100
num_samples = 10

#Generate random gene expression data for control and disease groups
control_group = np.random.normal(10, 2, (num_genes, num_samples))  # Control: mean=10, std=2
disease_group = np.random.normal(12, 2, (num_genes, num_samples))  # Disease: mean=12, std=2
