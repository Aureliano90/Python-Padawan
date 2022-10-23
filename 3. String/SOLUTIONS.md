## [Mutations](https://www.hackerrank.com/challenges/python-mutations/problem)

```python
def mutate_string(string, position, character):
    return string[:position] + character + string[position + 1:]
```

## [Capitalize!](https://www.hackerrank.com/challenges/capitalize/problem)

```python
def solve(s):
    res = ''
    head = True
    for c in s:
        if c == ' ':
            head = True
            res += c
        elif head:
            res += c.upper()
            head = False
        else:
            res += c
    return res
```

## [sWAP cASE](https://www.hackerrank.com/challenges/swap-case/problem)

```python
def swap_case(s: str):
    s = list(s)
    for i, c in enumerate(s):
        if c.isalpha():
            if c.islower():
                s[i] = c.upper()
            else:
                s[i] = c.lower()
    return ''.join(s)
```

## [What's Your Name?](https://www.hackerrank.com/challenges/whats-your-name/problem)

```python
def print_full_name(first, last):
    print(f"Hello {first} {last}! You just delved into python.")
```

## [String Formatting](https://www.hackerrank.com/challenges/python-string-formatting/problem)

```python
def print_formatted(number):
    width = len(f'{number:b}')
    for i in range(1, number+1):
        print(f'{i:{width}d}', f'{i:{width}o}', f'{i:{width}X}', f'{i:{width}b}')
```

## [Time Conversion](https://www.hackerrank.com/challenges/time-conversion/problem)

```python
def timeConversion(s):
    return f'{int(s[0:2]) + 12}' + s[2:len(s) - 2] if s.endswith('PM') and s[:2] != '12' else '12' + s[2:len(
        s) - 2] if not s.endswith('AM') else '00' + s[2:len(s) - 2] if s[:2] == '12' else s[:len(s) - 2]
```
