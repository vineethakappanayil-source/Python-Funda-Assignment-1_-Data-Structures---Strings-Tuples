# Python Fundamentals Assignment 1: Strings and Tuples

Step-by-step solutions for the Python Fundamentals assignment on strings and tuples.

## Contents

- [Requirements](#requirements)
- [1. String concatenation](#1-string-concatenation)
- [2. String slicing and indexing](#2-string-slicing-and-indexing)
- [3. String methods](#3-string-methods)
- [4. Tuples](#4-tuples)
- [Run the examples](#run-the-examples)

## Requirements

- Python 3
- A terminal or Python editor

## 1. String concatenation

Ask for a name, prepend `Hello `, then add the welcome phrase to the same string.

```pythonname = input("Enter your Name: ")
greeting = "Hello " + name
print(greeting)

full_string = greeting + ", welcome to Python programming"
print(full_string)

Example:

```text
Enter your Name: Zara
Hello Zara
Hello Zara, welcome to Python programming
```

`+` joins strings. The spaces and comma are included in the string literals so the output reads naturally.

## 2. String slicing and indexing

Continue with the `message` created above. Python indexes start at `0`; negative indexes count from the end. In a slice, the start is included and the stop is excluded.
s = full_string   # "Hello Zara, welcome to Python programming"
```python
print("First character:", s0])
print("Last character:", s[-1])
print("First 5 characters:",s[:5])
print("Last 11 characters:", s[-11:])
print("Reversed string:", s[::-1])

start =s.index("Python")
python_word = s[start:start + len("Python")]
print("Word Python:", python_word)
```

For the name `Zara`, this prints:

```text
First character: H
Last character: g
First 5 characters: Hello
Last 11 characters: programming
Reversed string: gnimmargorp nohtyP ot emoclew ,araZ olleH
Word Python: Python
```

- `s[0]` selects the first character; `message[-1]` selects the last.
- `s[:5]` selects characters from the beginning up to index `5`.
- s[-11] selects the final 11 characters.
- `s[::-1]` uses a step of `-1` to read the string backward.
- `.index("Python")` finds the word's starting position; the next slice extracts its six characters.

## 3. String methods

```python
strM = "Python beginner tutorial"

print("Uppercase:", strM.upper())
print("Lowercase:", strM.lower())
print("Capitalized:", strM.capitalize())
print("Number of t characters:", strM.count("t"))
print("Replaced:", strM.replace("Python", "Machine Learning"))
```

Output:

```text
Uppercase: PYTHON BEGINNER TUTORIAL
Lowercase: python beginner tutorial
Capitalized: Python beginner tutorial
Number of t characters: 2
Replaced: Machine Learning beginner tutorial
```

`capitalize()` makes the first character uppercase and the rest lowercase. The provided sentence already has that form, so its output matches the input. `count("t")` counts lowercase `t` characters, and `replace()` returns a new string with `Python` replaced.

## 4. Tuples

```python
tuple1 = (10, 20, 30)
tuple2 = (40, 50, 60)

t_combine = tuple1 + tuple2
print("Combined tuple:", t_combine)

repeated = t_combine * 3
print("Repeated 3 times:", repeated)

print("Third element:", t_combine[2])
print("First three elements:", t_combine[:3])
print("Last three elements:", t_combine[-3:])
```

Output:

```text
Combined tuple: (10, 20, 30, 40, 50, 60)
Repeated 3 times: (10, 20, 30, 40, 50, 60, 10, 20, 30, 40, 50, 60, 10, 20, 30, 40, 50, 60)
Third element: 30
First three elements: (10, 20, 30)
Last three elements: (40, 50, 60)
```

`+` concatenates tuples and `* 3` repeats their contents three times. The third element is at index `2`. Tuples are immutable, so concatenation and repetition create new tuples rather than modifying the originals.

## Run the examples

Copy each section into a `.py` file and run it with Python 3. The slicing section uses `message` from the string-concatenation section, so run those sections in order.
