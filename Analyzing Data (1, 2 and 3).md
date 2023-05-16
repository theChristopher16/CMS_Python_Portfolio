# MSNT 657: Analyzing Data (1, 2 and 3)
## Student Name: Christopher Smith
## Professor: Dr. Vandenbrink

1. 
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

2. 
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