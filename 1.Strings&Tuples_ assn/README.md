# Python Basics: Strings & Tuples

![Python](https://img.shields.io/badge/Python-3.x-blue?logo=python&logoColor=white)
![Jupyter](https://img.shields.io/badge/Jupyter-Notebook-orange?logo=jupyter&logoColor=white)

A practice notebook (`1_Strings_Tuples__assn.ipynb`) covering core operations on Python **strings** and **tuples**.

## Topics Covered

| Section | Concepts |
|---------|----------|
| String concatenation | `input()`, joining strings with `+` |
| String slicing | positive and negative indexing, ranges, reversing with `[::-1]` |
| String methods | `upper()`, `lower()`, `capitalize()`, `count()`, `replace()` |
| Tuple operations | concatenation, repetition, indexing, slicing |

## What Each Cell Does

**1. Greeting program**
Takes the user's name as input and prints a welcome message.

```text
enter your name = Bharat
Hello Bharat welcome to python programming
```

**2. Slicing**
Works on the string `"Hello Bharat welcome to python programming"`.

| Code | Result |
|------|--------|
| `str3[0]` | `H` (first character) |
| `str3[-1]` | `g` (last character) |
| `str3[0:5]` | `Hello` |
| `str3[0:11]` | `Hello Bhara` |
| `str3[::-1]` | the whole string reversed |
| `str3[-18:-12]` | `python` |

**3. String methods**
Applied to `"Python beginner tutorial"`.

| Method | Result |
|--------|--------|
| `upper()` | `PYTHON BEGINNER TUTORIAL` |
| `lower()` | `python beginner tutorial` |
| `capitalize()` | `Python beginner tutorial` |
| `count('t')` | `3` |
| `replace("Python", "Data Analytics")` | `Data Analytics beginner tutorial` |

**4. Tuples**
Uses `tup1 = (10, 20, 30)` and `tup2 = (40, 50, 60)`.

- Concatenation gives `(10, 20, 30, 40, 50, 60)`
- Repeating the combined tuple 3 times gives 18 elements
- `t_combine[:3]` gives `(10, 20, 30)`
- `t_combine[2]` gives `30`
- `t_combine[-3:]` gives `(40, 50, 60)`

## Key Takeaways

- Strings and tuples are **immutable**. Methods like `replace()` return a new string instead of changing the original.
- `count()` is case-sensitive, so `count('t')` does not count `T`.
- Negative indices count from the end, and `[::-1]` reverses a sequence.

## How to Run

```bash
jupyter notebook 1_Strings_Tuples__assn.ipynb
```

Run the cells in order. The first cell asks for your name.

## Requirements

Python 3.x and Jupyter Notebook. No external libraries are needed.
