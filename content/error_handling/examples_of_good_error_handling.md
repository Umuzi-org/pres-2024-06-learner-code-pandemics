## Examples of good error handling

```python
def divide(a, b):
    try:
        result = a / b
    except ZeroDivisionError as zero_div_error:
        raise(zero_div_error)
    except TypeError as type_error:
        raise(type_error)
    return result

print(divide(10, 0))  # Outputs: Error: Division by zero.
print(divide(10, 'a'))  # Outputs: Error: Inputs must be numbers.
print(divide(10, 2))  # Outputs: 5.0
```