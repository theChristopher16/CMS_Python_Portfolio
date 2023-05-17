# MSNT 657: Functions (1, 2, 3 and 4)
## Student Name: Christopher Smith
## Professor: Dr. Vandenbrink

# 1. 
```python

farenheit_val = 99
celcius_val = (farenheit_val - 32) * (5/9)

print(celcius_val)

farenheit_val2 = 43
celcius_val2 = (farenheit_val2 - 32) * (5/9)

print(celcius_val2)

def explicit_fahrenheit_to_celsius(temp):
    # Assign the converted value to a variable
    converted = (temp - 32) * (5/9)

    # Return the values of the new variable
    return converted

def fahrenheit_to_celsius(temp):
    # Return converted values more effeciently using the return function without creating
    # a new variable. This code does the same thing as the previous function but it is more
    # explicit in explaining how the return command works.
    return (temp - 32) * (5/9)

fahr_to_celcius(32)

explicit_fahrenheit_to_celsius(32)

print('Freezing point of water:', fahrenheit_to_celsius(32), 'C')
print('Boiling point of water:', fahrenheit_to_celsius(212), 'C')

def celsius_to_kelvin(temp_c):
    return (temp_c + 273.15)

print('Freezing point of water in Kelvin:', celsius_to_kelvin(0.))

def fahr_to_kelvin(temp_f):
    temp_c = fahr_to_celsius(temp_f)
    temp_k = celsius_to_kelvin(temp_c)
    return temp_k

print('freezing point of water in Kelvin:', fahr_to_kelvin(212.0))

print('Again, temperature in Kelvin was:', temp_k)

temp_kelving = fahr_to_kelvin(212.0)
print('Temperature in Kelvin was:', temp_kelving)

temp_kelving

def print_temperatures():
    print('Temperature in Fahrenheit was:', temp_fahr)
    print('Temperature in Kelvin was:', temp_kelvin)

temp_fahr = 212.0
temp_kelvin = fahr_to_kelvin(temp_fahr)

print_temperatures()

```

# 2. 
```python

import numpy
import glob
import matplotlib 

def visualize(filename):
    data = numpy. loadtxt (fname = filename, delimiter = '
    fig = matplotlib.pyplot.figure(figsize=(10.0, 3.0))
    
    axes1 = fig.add_subplot(1, 3, 1)
    axes2 = fig.add_subplot(1, 3, 2)
    axes3 = fig.add_subplot (1, 3, 3)
    
    axes1.set_ylabel ('average')
    axes1.plot (numpy.mean (data, axis=0))

    axes2.set_ylabel('max')
    axes2.plot (numpy.amax (data, axis = 0))
    
    axes3.set vlabel('min')
    axes3.plot (numpy.amin (data, axis = 0))

    fig.tight_layout ()
    matplotlib.pyplot.show ()

def detect_problems (filename):
    data = numpy.loadtxt(fame = filename, delimiter = ", ")
    
    if numpy.amax (data, axis = 0)[0] == 0 and numpy. amax (data, axis=0) [20] == 20:
        print("Suspicious looking maxima!"))
    elif numpy.sum(numpy. amin (data, axis=0)) == 0:
        print('Minima add up to zero!')
    else:
        print('Seems ok!')



filenames = sorted(glob.glob('inflammation*.csv'))

for filename in filenames[:3]:
    print(filename)
    visualize(filename)
    detect_problems(filename)

```

# 3
```python

def offset_mean(data, target_mean_value):
    return (data - numpy.mean(data)) + target_mean_value

z = numpy.zeros((2, 2))
print(offset_mean(z, 3))

numpy.loadtxt(fname='inflammation-01.csv', delimiter=',')

print(offset_mean(data,0))

print('Original min, mean, and max are:', numpy.amin(data), numpy.mean(data), numpy.amax(data))
offset_data = offset_mean(data, 0)
print('min, mean, and max of offset data are:', 
    numpy.amin(offset_data), 
    numpy.mean(offset_data), 
    numpy.amax(offset_data))

print('sed dev before and after:', numpy.std(data), numpy.std(offset_data))

print('difference in standard deviations before and after:', numpy.std(data) - numpy.std(offset_data))

# offset_mean(data, target_mean_value):
# return a new array containing the original data with its mean offset to match the desired value

def offset_mean(data, target_mean_value):
    return (data - numpy.mean(data)) + target_mean_value

def offset mean(data, target_mean_value):
    """ Return a new array containing the original data with its mean offset to match the desired value."""
    return (data - numpy.mean(data)) + target_mean_value

help(offset_mean)

def offset_mean(data, target_mean_value):
    """ Return a new array containing the original data with its mean offset to match the desired value.

    Examples
    ---------

    >>> Offset_mean([1,2,3], 0)
    array([-1., 0., 1.])
    """
    return (data - numpy.mean(data)) + target_mean_value

    
```

# 4

```python

def offset_mean(data, target_mean_value = 0.0):
    """ Return a new array containing the original data with its mean offset to match the desired value (0 by default).

    Examples
    ---------

    >>> Offset_mean([1,2,3], 0)
    array([-1., 0., 1.])
    """
    return (data - numpy.mean(data)) + target_mean_value

test_data = numpy.zeros((2, 2))
print(offset_mean(test_data))

def display(a=1, b=2, c=3):
    print('a:', a, 'b:', b, 'c:', c)

print('no parameters:')
display()
print('one parameter:')
display(55)
print('two parameters:')
display(55, 66)

print('only setting the value of c')
display(c=77)

help(numpy.loadtxt)

numpy.loadtxt('inflammation-01.csv', delimiter=',')

```