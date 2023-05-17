# MSNT 657: Functions (1, 2, 3 and 4)
## Student Name: Christopher Smith
## Professor: Dr. Vandenbrink

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
    return converted