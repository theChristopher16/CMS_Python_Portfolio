# MSNT 657: Analyzing Data (1, 2 and 3)
## Student Name: Christopher Smith
## Professor: Dr. Vandenbrink

# 1. 
```python
import numpy
numpy.loadtxt(fname='inflammation-01.csv', delimiter=',')

data = numpy.loadtxt(fname='inflammation-01.csv', delimiter=',')

print(data)
print(type(data))
print(data.shape)

print('first value in data:, data[0,0])
print('middle value in data:, data[29, 19])
print(data[0:4, 0:10])

print(data[5:10, 0:10])

small = data[:3, 36:]
print('small is:')
print(small)
```
# 2.
```python
# Lets use a numpy function
print(numpy.mean(data))

maxval, minval, stdval = numpy.max(data), numpy.min(data), numpy.std(data)

maxval = numpy.amax(data)
minval = numpy.amin(data)
stdval = numpy.std(data)

print(maxval)
print(minval)
print(stdval)

print('maximum inflammation:', maxval)
print('minimum inflammation:', minval)
```

# 3.
```python
import numpy
data = numpy.loadtxt(fname='inflammation-01.csv', delimiter=',')

import matplotlib.pyplot
image = matplotlib.pyplot.imshow(data)
matplotlib.pyplot.show()

# Average inflammation over time
ave_inflammation = numpy.mean(data, axis=0)
ave_plot = matplotlib.pyplot.plot(ave_inflammation)
matplotlib.pyplot.show()

max_plot = matplotlib.pyplot.plot(numpy.max(data, axis=0))
matplotlib.pyplot.show()

min_plot = matplotlib.pyplot.plot(numpy.min(data, axis=0))
matplotlib.pyplot.show()

fig = matplotlib.pyplot.figure(figsize=(10.0, 3.0))
axes1 = fig.add_subplot(1, 3, 1)
axes2 = fig.add_subplot(1, 3, 2)
axes3 = fig.add_subplot(1, 3, 3)

axes1.set_ylabel('average')
axes1.plot(numpy.mean(data, axis=0))

axes2.set_ylabel('max')
axes2.plot(numpy.max(data, axis=0))

axes3.set_ylabel('min')
axes3.plot(numpy.min(data, axis=0))

fig.tight_layout()

matplotlib.pyplot.savefig('inflammation.png')
matplotlib.pyplot.show()
```