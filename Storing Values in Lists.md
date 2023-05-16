odds = [1, 3, 5, 7]
print('odds are:', odds)

print('first element:', odds[0])
print('last element:', odds[3])
print('"-1" element:', odds[-1])

names = ['Curie', 'Darwing', 'Turing']

print('names is originally:', names)
names[1] = 'Darwin'
print('final value of names:', names)

<!-- name = 'Darwin'
name[0] = 'd' -->

odds.append(11)
print('odds after adding a value:', odds)

removed_element = odds.pop(0)
print('odds after removing the first element:', odds)
print('removed_element:', removed_element)

odds.reverse()
print('odds after reversing:', odds)

odds = [3, 5, 7]
primes = odds
primes.append(2)
print('primes:', primes)
print('odds:', odds)

odds = [3, 5, 7]
primes = list(odds)
primes.append(2)
print('primes:', primes)
print('odds:', odds)

binomial_name = 'Drosophila melanogaster'
group = binomial_name[0:10]
print('group:', group)

species = binomial_name[11:23]
print('species:', species)

<!-- chromosomes = ['X', 'Y', 'Z', '2', '3', '4'] -->
autosomes = chromosomes[2:5]
print('autosomes:', autosomes)

last = chromosomes[-1]
print('last:', last)

date = 'Monday 4 January 2023'
day = date[0:6]
print('Using 0 to begin range:', day)
day = date[:6]
print('Ommiting beginning index:', day)

months = ['jan', 'feb', 'mar', 'apr', 'may', 'jun', 'jul', 'aug', 'sep', 'nov', 'dec']

sond = months[8:12]
print('With known last position:', sond)

sond = months[8:len(months)]
print('Using len() to get last position:', sond)
sond = months[8:]
print('Omitting last position:', sond)