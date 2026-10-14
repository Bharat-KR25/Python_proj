# Python Basics: Lists, Dictionaries, Sets & Conditionals

![Python](https://img.shields.io/badge/Python-3.x-blue?logo=python&logoColor=white)
![Jupyter](https://img.shields.io/badge/Jupyter-Notebook-orange?logo=jupyter&logoColor=white)

A practice notebook (`2_Data_Structures__List__Dictionary__Set_-_Conditional_Statements.ipynb`) covering Python's main built-in data structures and `if / elif / else` logic.

## Topics Covered

| Section | Concepts |
|---------|----------|
| Lists | creation, `append`, `insert`, `remove`, `pop`, `extend`, `sort`, `max`, `min`, `sum`, indexing, slicing |
| Dictionaries | creation, key access, `update`, reassigning values, `keys()`, `values()`, `items()` |
| Sets | duplicate removal, `union`, `intersection`, why sets cannot be indexed |
| Conditionals | `if`, `elif`, `else` with a score checker |

## What Each Part Does

### 1. Lists

- `age_list = [24, 25, 27, 28, 29]`
- `name_list = ["Ram", "Rita", "Ragavi", "Joshua"]`

| Operation | Effect |
|-----------|--------|
| `append("Yazhini")` | adds an item to the end |
| `insert(2, 26)` | inserts `26` at index 2 |
| `remove("Yazhini")` | removes by value |
| `pop(3)` | removes by index |
| `extend([31, 30, 32])` | adds several items at once |
| `sort(reverse=True)` | sorts in descending order |

Statistics on `age_list`: **max = 32**, **min = 24**, **sum = 252**.

Indexing and slicing on `name_list` include the first element, the last element, a range slice, and the reversed list with `[::-1]`.

### 2. Dictionary

`students_marks` maps five student names to marks out of 100.

- Read a value: `students_marks["Vijay"]` returns `68`
- Add a student: `update({"Janani": 80})`
- Change a value: `students_marks["Rohit"] = 78`
- Inspect with `keys()`, `values()` and `items()`

### 3. Sets

- `my_set` shows that duplicates are removed automatically.
- Indexing a set (`my_set[4]`) raises an error because sets are unordered and have no index positions.
- `set1 = {1, 3, 5, 7, 9}` and `set2 = {2, 3, 5, 8, 10}` are combined with `union()` and `intersection()`.

### 4. Conditional Statements

Takes a score from the user and classifies it:

| Score | Output |
|-------|--------|
| greater than 7 | Above average |
| 4 to 7 | Average: Good effort! Keep practicing... |
| below 4 | Below Average |

```text
Enter your score(0 to 7) = 7
Average: Good effort! Keep practicing, there's room for improvement.
```

## Notes

- `keys()`, `values()`, `items()`, `union()` and `intersection()` are called without `print()`, so they show no output when run inside a script. Wrap them in `print()` to see the results (in Jupyter, only the last expression in a cell is displayed automatically).
- The score prompt asks for a value from 0 to 7, so the "Above average" branch (`score > 7`) is only reachable if the user enters a value outside that range.
- The `name_list` has four names, not five.

## How to Run

```bash
jupyter notebook "2_Data_Structures__List__Dictionary__Set_-_Conditional_Statements.ipynb"
```

Run the first cell. It ends with a prompt asking for a score.

## Requirements

Python 3.x and Jupyter Notebook. No external libraries are needed.
