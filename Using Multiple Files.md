# MSNT 657: Using Multiple Files
## Student Name: Christopher Smith
## Professor: Dr. Vandenbrink


```python
import glob

print(glob.glob('inflammation*.csv'))

import glob
import numpy
import matplotlib.pyplot

filenames = sorted(glob.glob('inflammation*.csv'))
filenames = filenames[0:3]

for filename in filenames:
    print(filename)
    data = numpy.loadtxt(fname=filename, delimiter=',')
    fig = matplotlib.pyplot.figure(figsize=(10.0, 3.0))

    axes1 = fig.add_subplot(1, 3, 1)
    axes2 = fig.add_subplot(1, 3, 2)
    axes3 = fig.add_subplot(1, 3, 3)

    axes1.set_ylabel('average')
    axes1.plot(numpy.mean(data, axis=0))

    axes2.set_ylabel('max')
    axes2.plot(numpy.min(data, axis=0))

    axes3.set_ylabel('min')
    axes3.plot(numpy.max(data, axis=0))

    fig.tight_layout()
    matplotlib.pyplot.show()
```