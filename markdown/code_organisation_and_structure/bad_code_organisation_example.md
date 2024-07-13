**Example of badly organized code**

```
def process_data(data):
    data.sort()
    filtered_data = [d for d in data if d % 2 == 0]
    total = sum(filtered_data)
    print("Total:", total)
    with open('output.txt', 'w') as f:
        f.write(str(total))

data = [5, 2, 9, 1, 5, 6]
process_data(data)
```