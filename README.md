# Codon Table Generator

A Python program that translates a DNA or RNA sequence into amino acids using the standard genetic code.

## What it does

- Stores all 64 codons and their amino acids in a dictionary
- Accepts a DNA sequence (A, T, G, C) or an RNA sequence (A, U, G, C)
- Checks that the input has only valid nucleotides
- Divides the sequence into codons of three nucleotides
- Translates each codon into its amino acid
- Identifies start codons (ATG / AUG) and stop codons (TAA, TAG, TGA / UAA, UAG, UGA)
- Handles an incomplete codon at the end of the sequence (it is shown but not translated)
- Displays the full codon table and the translation result

The RNA codon table is built from the DNA table by replacing T with U.

## How to run

```
python codon_table_generator.py
```

Choose 1 for DNA or 2 for RNA, then enter the sequence.

## Sample

Input:

```
ATGGCTTTTTAA
```

Output:

| Item | Result |
|---|---|
| Codons | ATG - GCT - TTT - TAA |
| Amino acids | Methionine - Alanine - Phenylalanine - Stop |
| Start codon | ATG |
| Stop codon | TAA |
| Incomplete codon | None |

RNA example: `AUGGCUUUUUAAG` gives AUG - GCU - UUU - UAA, with `G` left as an incomplete codon.

## Comparison with a standard codon table

The dictionary was compared with the standard genetic code table (NCBI table 1) from Biopython (`Bio.Data.CodonTable`). All 64 codons and their amino acids (including the 3 stop codons) match.

## Concepts used

Python dictionaries, loops, conditional statements, string manipulation, input validation, basic biological sequence analysis.
- Python 3
- No extra libraries are needed
# Commit 4
A "README.md" @'

## Requirements

- Python 3
- No extra libraries are needed
## RNA example

Input (choose option 2):

AUGGCUUUUUAAG

Codons: AUG - GCU - UUU - UAA
Amino acids: Methionine - Alanine - Phenylalanine - Stop
Incomplete codon: G
## Author

Deekshith M
MSc Bioinformatics and Biotechnology, Chanakya University, Bengaluru