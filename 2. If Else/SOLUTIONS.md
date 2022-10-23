## [Finding the percentage](https://www.hackerrank.com/challenges/finding-the-percentage/problem)

```python
if __name__ == '__main__':
    n = int(input())
    student_marks = {}
    for _ in range(n):
        name, *line = input().split()
        scores = list(map(float, line))
        student_marks[name] = scores
    query_name = input()
    
    print(f'{sum(student_marks[query_name])/len(student_marks[query_name]):.2f}')
```

## [Find the Runner-Up Score!](https://www.hackerrank.com/challenges/find-second-maximum-number-in-a-list/problem)

```python
if __name__ == '__main__':
    n = int(input())
    arr = list(map(int, input().split()))
    arr.sort(reverse=True)
    for i in arr:
        if i != arr[0]:
            print(i)
            break
```

## [Write a function](https://www.hackerrank.com/challenges/write-a-function/problem)

```python
def is_leap(year):
    return True if not year % 400 else False if not year % 100 else False if year % 4 else True
```

## [Bill Division](https://www.hackerrank.com/challenges/bon-appetit/problem)

```python
def bonAppetit(bill, k, b):
    print('Bon Appetit' if (i := (sum(bill) - bill[k]) // 2) == b else b - i)
```
