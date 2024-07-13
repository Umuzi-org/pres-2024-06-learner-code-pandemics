## Examples of good error handling

```python
def divide(a, b):
    try:
        result = a / b
    except ZeroDivisionError:
        print("Error: Division by zero is not allowed.")
        return None
    except TypeError:
        print("Error: Inputs must be numbers.")
        return None
    return result

print(divide(10, 0))  # Outputs: Error: Division by zero is not allowed.
print(divide(10, 'a'))  # Outputs: Error: Inputs must be numbers.
print(divide(10, 2))  # Outputs: 5.0
```