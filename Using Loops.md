# MSNT 657: Using Loops
## Student Name: Christopher Smith
## Professor: Dr. Vandenbrink

```python
odds = [1, 3, 5, 7]
print(odds[0])
print(odds[1])
print(odds[2])
print(odds[3])

odds = [1, 3, 5]
print(odds[0])
print(odds[1])
print(odds[2])
print(odds[3])

odds = [1, 3, 5, 7, 9,  11, 13, 15, 17, 19]

for num in odds:
    print(num)

length = 0
names = ['Curie', 'Darwin', 'Turing']
for name in names:
    length = length + len(name)
print('There are', length, 'letters in the list.')

name = "Rosalind"
for name in ['Curie', 'Darwin', 'Turing']:
    print(name)
print('after the loop, name is', name)

print(len([0, 1, 2, 3]))

names = ['Curie', 'Darwin', 'Turing']
print(len(name))

```