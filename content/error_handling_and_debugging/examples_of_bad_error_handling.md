## Examples of bad error handling

```
def divide(a, b):
    try:
        result = a / b
    except:
        print("Something went wrong.")
    return result

print(divide(10, 0))  # Outputs: Something went wrong. Followed by a crash due to undefined 'result'
```