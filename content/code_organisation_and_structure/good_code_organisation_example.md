### Good code organization example

```python
def sort_data(data):
    return sorted(data)

def filter_even(data):
    return [d for d in data if d % 2 == 0]

def save_to_file(total, filename):
    try:
        with open(filename, 'w') as f:
            f.write(str(total))
    except IOError:
        print(f"Error saving to {filename}")

def process_data(data, filename='output.txt'):
    sorted_data = sort_data(data)
    even_data = filter_even(sorted_data)
    total = sum(even_data)
    print("Total:", total)
    save_to_file(total, filename)

data = [5, 2, 9, 1, 5, 6]
process_data(data)
```

Notice that the functions are not stored in a saperate file :)