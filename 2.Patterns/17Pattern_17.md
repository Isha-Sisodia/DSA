https://takeuforward.org/plus/dsa/problems/pattern-17
```python
n = 5

for i in range(1, n + 1):

    # Print spaces
    for j in range(n - i):
        print(" ", end="")

    # Increasing letters
    for j in range(i):
        print(chr(65 + j), end="")

    # Decreasing letters
    for j in range(i - 2, -1, -1):
        print(chr(65 + j), end="")

    print()
```
