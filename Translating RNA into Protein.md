# MSNT 657: Translating RNA into Protein
## Student Name: Christopher Smith
## Professor: Dr. Vandenbrink

```python

# Prompt the user to enter the input RNA file name
input_file_name = input('Enter the name of the input RNA file: ')

# Open the input RNA file and read the RNA sequence

with open(input_file_name, "r") as input_file:
    rna_sequence = input_file.read().strip()

# Define the codon table
codon_table = {
    “UUU”:”F”, “UUC”:”F”, “UUA”:”L”, “UUG”:”L”,
    “UCU”:”S”, “UCC”:”S”, “UCA”:”S”, “UCG”:”S”,
    “UAU”:”Y”, “UAC”:”Y”, “UAA”:””, “UAG”:””,
    “UGU”:”C”, “UGC”:”C”, “UGA”:””, “UGG”:”W”,
    “CUU”:”L”, “CUC”:”L”, “CUA”:”L”, “CUG”:”L”,
    “CCU”:”P”, “CCC”:”P”, “CCA”:”P”, “CCG”:”P”,
    “CAU”:”H”, “CAC”:”H”, “CAA”:”Q”, “CAG”:”Q”,
    “CGU”:”R”, “CGC”:”R”, “CGA”:”R”, “CGG”:”R”,
    “AUU”:”I”, “AUC”:”I”, “AUA”:”I”, “AUG”:”M”,
    “ACU”:”T”, “ACC”:”T”, “ACA”:”T”, “ACG”:”T”,
    “AAU”:”N”, “AAC”:”N”, “AAA”:”K”, “AAG”:”K”,
    “AGU”:”S”, “AGC”:”S”, “AGA”:”R”, “AGG”:”R”,
    “GUU”:”V”, “GUC”:”V”, “GUA”:”V”, “GUG”:”V”,
    “GCU”:”A”, “GCC”:”A”, “GCA”:”A”, “GCG”:”A”,
    “GAU”:”D”, “GAC”:”D”, “GAA”:”E”, “GAG”:”E”,
    “GGU”:”G”, “GGC”:”G”, “GGA”:”G”, “GGG”:”G”
}

# Translate RNA into protein

protein_sequence = " "
for i in range(0, len(rna_sequence), 3):
    codon = rna_sequence[i:i+3]
    if len(codon) == 3:
        amino_acid = codon_table[codon]
        if amino_acid == "":
            break
        protein_sequence += amino_acid

# Prompt the user to enter the output file name

output_file_name = input('Enter the name of the output file: ')

# Save the protein sequence to a text file

with open(output_file_name, 'w') as output_file:
    output_file.write(protein_sequence)
    print(f"The sequence has been saved to {output_file_name}")

print(protein_sequence)

```