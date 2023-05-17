# MSNT 657: Transcribing DNA into RNA
## Student Name: Christopher Smith
## Professor: Dr. Vandenbrink

```python
# Prompt the user to enter the input fasta file name

input_file_name = input('Enter the name of the input fasta file: ')

# Open the input fasta file and read the DNA sequence

with open(input_file_name, 'r') as input_file:
    dna_sequence = ""
    for line in input_file:
        if line.statswith('>'):
            continue
        dna_sequence += line.rstrip()

# Transcribe the DNA sequence into RNA
rna_sequence = ""
for nucleotide in dna_sequence:
    if nucleotide == 'T':
        rna_sequence += 'U'
    else:
        rna_sequence += nucleotide

# Prompt the user to enter the output file name

out_file_name = input('Enter the name of the output file: ')

# Save the RNA sequence to a text file

with open(output_file_name, 'w') as output_file:
    output_file.write(rna_sequence)
    print(f"The sequence has been saved to {output_file_name}")

print(rna_sequence)

```