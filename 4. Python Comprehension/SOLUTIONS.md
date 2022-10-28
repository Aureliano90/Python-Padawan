## [Staircase](https://www.hackerrank.com/challenges/staircase/problem)

```python
def staircase(n):
    print(*[' ' * (n - i - 1) + '#' * (i + 1) for i in range(n)], sep='\n')
```

## [Plus Minus](https://www.hackerrank.com/challenges/plus-minus/problem)

```python
def plusMinus(arr):
    print(f'{len([x for x in arr if x > 0]) / len(arr):.6f}', f'{len([x for x in arr if x < 0]) / len(arr):.6f}', f'{len([x for x in arr if x == 0]) / len(arr):.6f}', sep='\n')
```

## [Compare the Triplets](https://www.hackerrank.com/challenges/compare-the-triplets/problem)

```python
def compareTriplets(a, b):
    return [sum([sign * a[i] > sign * b[i] for i in range(len(a))]) for sign in [1, -1]]
```

## [Sequence Equation](https://www.hackerrank.com/challenges/permutation-equation/problem)

```python
def permutationEquation(p):
    return sorted(range(1, len(p) + 1), key=lambda y: p[p[y - 1] - 1])
```

## [List Comprehensions](https://www.hackerrank.com/challenges/list-comprehensions/problem)

```python
if __name__ == '__main__':
    x, y, z, n = int(input()), int(input()), int(input()), int(input())
    print([[i, j, k] for i in range(x+1) for j in range(y+1) for k in range(z+1) if i+j+k != n])
```

## [Nested Lists](https://www.hackerrank.com/challenges/nested-list/problem)

```python
if __name__ == '__main__':
    records = sorted([tuple(reversed((input(), float(input()))) ) for _ in range(int(input()))])
    print('\n'.join([r[1] for r in records if r[0] == sorted(set([r[0] for r in records]))[1]]))
```
