# <font color="blue">Task 1: Basics of Python (60%)</font>

### Task 1.1:
#### Objective
##### Write a Python script to process a DNA sequence provided by the user. Your script should:

- Accept user input for a DNA sequence.
- Validate the sequence to ensure it only contains valid nucleotide bases (A, T, C, G).
- Convert the sequence to uppercase (to handle case insensitivity).
- Count the occurrences of each nucleotide (A, T, C, G) and display the results. Example: Counts for 'A'=50.
- Calculate and print the GC-content of the sequence (percentage of G and C bases). Example: CG content=100%.

##### Evaluation Criteria
- You can use a while loop to repeatedly ask for input if validation fails.
- Use a dictionary to store counts of each nucleotide for easy access and display.
- Format the GC-content percentage using Python's f-string formatting. GC content retains two decimal places.
- Correct use of Python basics (input, print, loops, and conditionals).
- Proper data validation and error handling.
- Clear and readable code with comments explaining each section.
- Accurate calculation of nucleotide counts and GC-content.

Input DNA sequence, <font color="green"> Length of DNA is 1047 </font>: '''<sequence: TGGCGCCCCCGACAGCCATGCGTACGGCAGGCCACAAGCCGTGGCGCGACCGACCACAGCGTGTCGGCGCTTTACGCGCGGCCGGACGGGACCTGGCAGGGCGAGGTTGTGTGGGCTGAGCCGCCGG  CTGCCCGGGAGCGGGCGGCAGCGGGGGGAACGGCGGGGATGAGCGGCCGCGCCGCCCGGCCCCCCCGGTACGCAGCAAGCCCGCCCTCGTCACGCGGGGTCCGGGGCAGGGTGGGGCAGGCGCTCCC  GTCGCCCGGCACGCTTGTGTCGGCGCTCGTTGGCGCCGGACCAGGCGGGTCAGCGGAAGGGCTGACCCGTGTGCCCGCCGGTTCCCGCAAGTGGCGGGCATCGCCCTGTCCGCCTGGGTCAGGGCAC  ACTATGCGGGGGAGTAGCTCGGAGTCTACCATTCGTTCGAGCGTCGCGCAGGAACATCGTCGAGCGCCCCCTCCCCTGAGCGCTCGCGGCCTTGGGCCCACGCCAGGGGGATCCCTCCTACGGCCGC  CCCGCCTGGGTAGCAACGCTGCGGCAACCGGGCGCCCGGAGCGCGAGTCACGTAGTGGGTCTACTTGGCCCGGGCCTGGATGGCGGGGCAGCCCCTCGCCCACCCGCCTCCCGCCCCGCCCCCCTGC  GTTACGCGGGGCCGGAGCGCTCGGCGGCGGGGCCGCGCACGGCCACCGCGCAGCGCGGCGGTcCGAGCGATCCGGCCGTCCCACGGCTGCCGGTGTCAGTCCAGTGCGTTCCGGGCTGGGGGACGAA  CACTGCGCTCCAAGTGGCAGGAGGGCTTCGGCCAGGCCGGCATTCCCCTGCCGAGCAGCTACCAGGGCACTACCAGGCCCGGCGGGCACGACCGCCCATTCGGTCCCCCGCGCTCGGCGCGATCGCG  AGCGGAGGCGAGCTCTGGCCGCGCCAGTAGCTCGCCCGGGGAGGCAGCATCGGCAGCCCCTAGCGATCCGGGAGCGGGGCAGGCGCGCCACGCCAGTAGCTCGCCCGGGGAGGCAGCATCGGCAGCC  CCTAGCGATCCGCTCGATAGTCGCGCGGGCG>'''

### Task 1.2: 

#### DNA Sequence Analysis
##### Problem Statement:
You are given a DNA sequence, a string composed of the characters 'A', 'T', 'C', and 'G'. Your task is to write a Python program that performs the following operations:

DNA sequence, <font color="green">Length of DNA sequence is 475 </font>: < ATCGATCGAACATCGATCATCATCGATCGAACATCGATCATCGATCGAAATCGATCGAACCGAACGATCGATCGAACATATCGATATCGATCGAACCGATCGAACATCGAACCATCGATCGAAATCG  ATCGAACCGAACGATCGATCGAACATATCGATATCGATCGAACCGATCGATCGAACATCGATCATCGATCGAAATCGATCGAACCGAACGATCGATCGAACATATCGATATCGATCGAACCGATCGA  ACATCGAACCATCATCGAACATCGAAATCGATCGAACATCGATCATCGATCGAAATCGATCGAACCGAACGATCGATCGAACATATCGATATCGATCGAACCGATCGAACATCGAACCATCCCATCA  TCGATCGAACATCGATCATCGATCGAAATCGATCGAACCGAACGATCGATCGAACATATCGATATCGATCGAACCGATCGAACATCGAACCATC  > 

1. Frequency Count: Count the frequency of each nucleotide ('A', 'T', 'C', 'G') in the sequence.
2. Reverse Complement: Generate the reverse complement of the DNA sequence. In DNA, 'A' pairs with 'T' and 'C' pairs with 'G'. The reverse complement is formed by reversing the sequence and swapping each nucleotide with its pair.
3. Find Subsequence: Write a function that takes a subsequence ('ATC') as input and returns the starting indices of any occurrences of this subsequence in the DNA sequence.

##### Evaluation Criteria
- frequency_count uses a dictionary for efficient counting.
- reverse_complement uses a comprehension for concise and efficient computation.
- find_subsequence demonstrates basic string manipulation and search techniques.
- Your solution should be efficient and well-commented to explain your logic.

<font color="blue"> Hint: the task expect you use the suitable data structure </font>

### Task 1.3: 
##### DNA Sequence Mutation Analysis
##### Problem Statement:

You have a DNA sequence represented as a string of characters 'A', 'T', 'C', 'G'. Your task is to write a Python program that performs the following analysis:

DNA sequence, <font color="green">Length of sequence is 700</font>: < ACTAACATCCAGTTAATAATTTATACATAGTTTAAGAATATACTACATTAAAAATACGAACTAAGACTGTATTACGCTCCCATCTAATCTATATTTTGTGTTCTATAAGATCCTTTATTAATATAG  TATACACTGTAATTATTACAACCAATCTGTGTAAGTAGGTTAATGCGATATTTGTTTGTTCTAAATCAATGATAACGTATAATTTCTATTATTCTAAATTCTCTCCTATCTGTCTATTTCAGCAGG  ATAAAGATAGAGGTATTCTTCCAATGTTTAATAATATGATAGTATCAATTATAAGTGGAATTTGTAATTAATTACCTATCAATTTCTACGATGATATGTCAGGACCCCTCGTAAACCGCTTCGTAA  TTTTAAAACGTACCATTGTTAATATCCGTGAGCGTTATGAAACTAGGTCGCTACCTGAATTATTGTcAcATGTTTTGCGTGAAAATCGTAGTTCGAATTGTCTTTAATAAGTCTTGTCAATTCGAA  CGTATACTCTTAAACTAAAAGGAATGAATTAAGAAAGTACAATTCAATACGTACGAAATAATAAAACCCGATCGCGTGATGCGTTCCCGAAATTTGGTAACAGTGACAACATACGACAACATATTT  GTGGGTATTAATCCTTTATAAGTCTTCTATATATGATTAGAAATAACAGATGTAACCAATAATTGCTAAA >

1. Validate Sequence: Check if the DNA sequence is valid (contains only 'A', 'T', 'C', 'G') using a for loop and if statements. If invalid, return an error message.
2. According to the error message returned, sort out the DNA sequence and re-analyze it.
3. Count Nucleotide Runs: Count the longest consecutive run of a given nucleotide ('A') in the sequence using a while loop.
4. Find Mutations: Identify all the positions in the DNA sequence where a mutation can result in a specific new nucleotide. You will be given a target nucleotide('G'), and you need to find the positions where changing the original nucleotide to the target nucleotide('G') is possible (Possible Mutation Positions for 'G').

### Task 1.4: 

### Debugging

#### Background: 
You are given a Python script that is intended to analyze a DNA sequence. The script takes a DNA string as input and calculates the frequency of each nucleotide (A, T, C, G). It also attempts to find the <font 'red'>'most common triplet' (set of three nucleotides, e.g., ATG, TGC) in the sequence. Capable of capturing all possible triplets.

DNA sequence,<font color="green"> Length of DNA sequence </font>: 490 : < AAAATACAATGTACATTCTTCGTATTATAGACATTTAGCTTAAAAATATACCAAAGATTTAATTTTATATTAATACATCAATATTTAATCTGCTGTATATGCGTTTATTTATAGGGGATGGAAATAT  ACTTAGTCATTATAAAGAAAATTTTGCTTGATATAATTATGACATATAAGTCTGTACAAATCACTTGATTTATTTGACACAATGCCAGCTCAAGTAATGACTATTTGGTACATCTTAAGAAAGAGTA  AGCCGGACTTTGAGGACAGAAAAATACATTCATATATCATTCGATTTATTTTTCTTATTTACCTTTTTTAGGACCTTATTTATAATTAAAATCAAAAAAAAAATCTTTCAAAGTTACAAAAAGGACA  ACTTTATACTATAAAGTATACCTTTTTTAATTAAATAAGTTATACAAGAATTATACCATTAACTCACAAACAGCTTATAAATACTTGATTAATTGACTAGATTCATTTT >

#### Task: 
The script is not functioning as expected. Your task is to debug the script, ensuring that it accurately calculates nucleotide frequencies and correctly identifies <font color="red">the most common triplet</font> in the DNA sequence.

#### Issues Reported:

1. The nucleotide frequency sometimes returns incorrect counts.
2. The most common triplet function does not always return the correct triplet.

#### Instructions:

1. Debug the provided script to fix the reported issues.
2. Explain the bugs you found and how you resolved them.
3. Provide a corrected version of the script.
4. Test the script with the provided DNA sequence and at least one other sequence of your choice.

#### Evaluation Criteria:

1. Accuracy in identifying and fixing the bugs.
2. Quality of the explanation provided for each bug and its solution.
3. The script should work correctly with any valid DNA sequence.
4. Code readability and documentation.

##### Explanation of Fixes

###### Nucleotide Frequency Bug:
- Added a conditional check in nucleotide_frequency to only count valid characters (A, T, C, G).

###### Most Common Triplet Bug:
- Changed the triplet loop to consider overlapping triplets by iterating from 0 to len(dna) - 2.

###### Validation:
- Added the validate_dna function to ensure the input DNA sequence only contains valid nucleotides.

###### Error Handling:
- Used try-except blocks to catch invalid sequences and provide helpful error messages.

###### Documentation and Readability:
- Added docstrings and comments for each function to explain its purpose.

# <font color="blue">Task 2: Advance of Python (40 points)</font>

### Task 2.1:(20%)

#### Task Description: DNA Analysis, Alignment, and Phylogenetic Tree Construction

#### Background
DNA sequence analysis is a critical part of bioinformatics. This task involves processing DNA sequences to analyze their transcription and translation, perform sequence alignments, and construct phylogenetic trees to study evolutionary relationships.

#### Objective
The goal of this task is to:
- Analyze DNA sequences from a FASTA file.
- Transcribe DNA to RNA.
- Translate RNA to proteins.
- Calculate the frequency of each amino acid in the proteins.
- Perform pairwise alignment between the first two sequences.
- Conduct multiple sequence alignment (MSA) for all sequences.
- Construct a phylogenetic tree based on the alignment.

##### Instructions
- Input File:'sequences 2.1.fasta'
A FASTA file containing DNA sequences. Each sequence will be identified by a unique sequence ID.

###### Steps to Implement: 
- Step 1: DNA Sequence Analysis
- For each sequence in the FASTA file:
- Transcribe the DNA sequence into RNA.
- Translate the RNA sequence into a protein sequence.
- Calculate and display the frequency of each amino acid in the protein.
- Output the DNA, RNA, protein sequences, and amino acid frequencies.

Step 2: Pairwise Alignment
- If there are at least two sequences:
- Perform a global pairwise alignment of the first two sequences.
- Display the alignment result, including aligned sequences and alignment score.

Step 3: Multiple Sequence Alignment
- Align all sequences in the FASTA file to create a multiple sequence alignment (MSA).
- Output the MSA.

Step 4: Phylogenetic Tree Construction
- Based on the MSA:
- Calculate a distance matrix.
- Construct a phylogenetic tree using the Neighbor-Joining method.
- Display or visualize the tree.
    
###### Output:
- DNA, RNA, and protein sequences for each entry.
- Amino acid frequencies.
- Pairwise alignment results.
- Multiple sequence alignment (MSA).
- Phylogenetic tree (ASCII representation).

##### Deliverables
1. A Python script that implements all the above steps using Biopython.
2. Example input file (sequences 2.1.fasta).
3. Example output showing:
- Sequence analysis results.
- Pairwise alignment.
- Multiple sequence alignment.
- Phylogenetic tree.

##### Evaluation Criteria
1. Functionality:
- Does the script correctly process and analyze DNA sequences?
- Are alignments and phylogenetic trees generated accurately?
2. Code Quality:
- Is the code modular, readable, and well-documented?
3. Output:
- Is the output comprehensive and easy to understand?
4. Efficiency:
- Does the script execute efficiently for the given dataset?

### Task 2.2: (20%)

### Task Description
The goal of this task is to analyze a cancer-associated skeletal muscle wasting dataset consisting of 1H-NMR urine metabolite data.The following parts are implemented in Python:

1. Data preparation
- Based on <font color="red">[All metabolites in dataset]</font>
- Load and clean the data.
- Check the basic structure of the data (such as missing values, column names, data types, etc.).
- Generate data descriptive statistics.

2. Data visualization
######   Based on <font color="red">[Table 4 Bivariate analysis: top 30 urine metabolites related to skeletal muscle loss]</font>
######  Basic distribution:
- Visualize the distribution of metabolite concentrations (such as histograms or box plots).
- Visualize the distribution of the target variable (whether it is associated with skeletal muscle wasting).
######  Correlation analysis:
- Use heatmap to visualize the correlation between metabolites.
- Dimensionality reduction:
- Use PCA (principal component analysis) to reduce the dimension of metabolite data and draw scatter plots of the first two principal components.
3. Build a simple machine learning model
######   Based on <font color="red">[Table 4 Bivariate analysis: top 30 urine metabolites related to skeletal muscle loss]</font>
Use metabolite data to predict whether skeletal muscle wasting is associated with cancer.
- Process:
- Separate features and target variables.
- Data partitioning: training set and test set.
- Choose a simple model (You can choose any model).
- Train the model and evaluate its performance (such as accuracy, ROC curve).

### Implementation description
1. Data description
- Load data and provide basic statistics.
- Display missing values ​​in data.
2. Data visualization
- Distribution map: Display the distribution of metabolites.
- Heat map: Visualize the correlation between metabolites.
- PCA: Draw the distribution of main components after dimensionality reduction.
3. Machine learning
- Model: You choosed machine learning model is used to predict whether skeletal muscle loss is related to cancer.
### Evaluation:
- Classification report (accuracy, precision, recall, etc.).
- ROC curve and AUC value.

### Evaluation criteria: The model does not need to be highly accurate, but it needs to have corresponding output results

