# Week 10

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

## Analyzing Protein Sequences

#### Calculate the molecular weight and isoelectric point of a protein sequence.


#### Molecular weight of a protein sequence
The molecular weight of a protein sequence is determined by the combined weights of all the amino acids that make up the protein, plus the weight of the water molecules that are released during the formation of peptide bonds. Each amino acid has a specific molecular weight, and these weights can be summed to calculate the total molecular weight of the protein.

The general steps to calculate the molecular weight of a protein from its sequence are:

1. Identify the Amino Acids: 
Break down the protein sequence into its constituent amino acids.

2. Calculate Individual Weights: 
Determine the molecular weight of each amino acid. This typically includes the weight of the amino acid minus the weight of one water molecule (18 daltons), which is lost during peptide bond formation.

3. Sum the Weights: 
Add up the weights of all the amino acids in the sequence.
4. Adjust for Terminal Amino Acids: 
Add back the weight of one water molecule (18 daltons) since the N-terminal and C-terminal amino acids do not lose a water molecule.

### Calling the BioPython module can implement the corresponding functions.

#### The isoelectric point (pI) of a protein

The isoelectric point (pI) of a protein is the pH at which the protein has no net electrical charge. At the isoelectric point, the protein is least soluble in water and may precipitate out of solution. The pI depends on the relative amounts of acidic (negatively charged) and basic (positively charged) amino acids in the protein.

To calculate the isoelectric point of a protein from its sequence:

1. Identify Charged Amino Acids: Determine the number of acidic (like aspartic acid, glutamic acid) and basic (like lysine, arginine, histidine) amino acids in the protein sequence.

2. Consider Terminal Amino Groups: The N-terminus and C-terminus of the protein also contribute to its overall charge. The N-terminus is typically considered as a basic group, and the C-terminus as an acidic group.

3. Use pKa Values: Each type of charged amino acid, as well as the terminal groups, has a characteristic pKa value, which is the pH at which half of the molecules of that amino acid are deprotonated.

4. Calculate Charge at Different pH Levels: The charge of the protein at different pH levels can be calculated using the pKa values and the Henderson-Hasselbalch equation.

5. Find the pH Where Net Charge is Zero: The pH at which the sum of all charges (positive and negative) equals zero is the isoelectric point.

### Calling the BioPython module can implement the corresponding functions.

1. Import necessary modules from Biopython.

2. Define a protein sequence.

3. Calculate the molecular weight of the protein.

4. Calculate the isoelectric point of the protein.

5. Print the results.

# Task 2

#### Parsing GenBank Files
Extract gene names and their sequences from a GenBank file.

genbank_file = "ls_orchid.gbk"  #Replace with your GenBank file

# Task 3 

#### Transcription and Translation of a DNA Sequence
Objective: Transcribe and translate a given DNA sequence.


1. Import the Seq class from Biopython.

2. Define a DNA sequence.

3. Transcribe the DNA sequence to RNA.

4. Translate the RNA sequence to a protein sequence.

5. Print the RNA and protein sequences.

#Defining a DNA sequence
dna_seq = Seq("ATGGCCATTGTAATGGGCCGCTGAAAGGGTGCCCGATAG")

# Task 4

#### Finding Restriction Sites
Objective: Identify the locations of restriction sites for a given enzyme in a DNA sequence.

1. Import necessary modules from Biopython.

2. Define a DNA sequence.

3. Use a restriction enzyme (EcoRI) to find its restriction sites in the DNA sequence.

4. Print the positions of the restriction sites.

### Restriction Enzymes
##### Definition: 
Restriction enzymes, also known as restriction endonucleases, are enzymes that cut DNA at or near specific recognition sequences, known as restriction sites. These enzymes are naturally found in bacteria, where they serve as a defense mechanism against invading viruses (bacteriophages).
##### Function: 
Each restriction enzyme recognizes a specific sequence of nucleotides (usually 4 to 8 bases long) and cleaves the DNA at or near this site. The cutting can result in 'blunt' or 'sticky' ends.
### Restriction Sites
##### Recognition Sequences: 
A restriction site is a specific sequence of DNA that is recognized and cut by a restriction enzyme. For example, the restriction enzyme EcoRI recognizes the sequence 5'-GAATTC-3' and cuts between G and A.
##### Palindromic Sequences: 
Most restriction sites are palindromic, meaning the sequence of nucleotides reads the same forward and backward on complementary strands. For instance, the EcoRI site GAATTC on one strand is complemented by CTTAAG on the opposite strand, which also reads GAATTC when read in the opposite direction.

#Defining a DNA sequence
dna_seq = Seq("GAATTCCGGATTAAGCTTGAATTC")

## Task 5: Pairwise Sequence Alignment

Objective: Perform a pairwise sequence alignment between two sequences.

1. Import necessary functions from the Biopython pairwise2 module.

2. Define two DNA sequences.

3. Perform global alignment between these two sequences.

4. Print all possible alignments.

#Defining two DNA sequences
seq1 = Seq("ACCGT")
seq2 = Seq("ACG")
