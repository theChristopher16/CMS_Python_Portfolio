# MSNT 657: Making Choices
## Student Name: Christopher Smith
## Professor: Dr. Vandenbrink

```python
num = 37
if num > 100:
    print('greater')
else:
    print('not greater')
print('done')

num = 53
print('before conditional...')
if num > 100:
    print(num, 'is greater than 100')
print('...after conditional')

num = -3

if num > 0:
    print(num, "is positive")
elif num == 0:
    print(num, "is zero")
else:
    print(num, "is negative")

if (1 > 0) and (-1 > 0):
    print('both parts are true')
else:
    print('at least one part is false')

if (1 < 0) or (-1 < 0):
    print('at least one test is true')
else:
    print('both of these are false')

import numpy

numpy.loadtxt(fname='inflammation-01.csv', delimiter=',')

max_inflammation_0 = numpy.amax(data, axis=0)

max_inflammation_20 = numpy.amax(data, axis=0)[20]

if max_inflammation_0 == 0 and max_inflammation_20 == 20:
    print('Suspicious looking maxima!')
elif numpy.sum(numpy.min(data, axis=0)) == 0:
    print('Minima add up to zero!')
else:
    print('Seems OK!')

data = numpy.loadtxt(fname='inflammation-01.csv', delimiter=',')

max_inflammation_0 = numpy.amax(data, axis=0)[0]

max_inflammation_20 = numpy.amax(data, axis=0)[20]

if max_inflammation_0 == 0 and max_inflammation_20 == 20:
    print('Suspicious looking maxima!')
elif numpy.sum(numpy.min(data, axis=0)) == 0:
    print('Minima add up to zero! -> HEALTHY PARTICIPANT ALERT!')
else:
    print('Seems OK!')
