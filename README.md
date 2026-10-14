# Python Fundamentals

![Python](https://img.shields.io/badge/Python-3.x-blue?logo=python&logoColor=white)
![Jupyter](https://img.shields.io/badge/Jupyter-Notebook-orange?logo=jupyter&logoColor=white)
![Dependencies](https://img.shields.io/badge/dependencies-none-brightgreen)

A collection of Jupyter notebooks built while learning Python. They start with basic data types and build up to a complete mini project that combines everything.

## Table of Contents

- [Projects at a Glance](#projects-at-a-glance)
- [1. Strings & Tuples](#1-strings--tuples)
- [2. Data Structures & Conditionals](#2-data-structures--conditionals)
- [3. Loops & Functions](#3-loops--functions)
- [4. Support Ticket Analyzer](#4-support-ticket-analyzer)
- [Skills Demonstrated](#skills-demonstrated)
- [Getting Started](#getting-started)
- [Repository Structure](#repository-structure)

## Projects at a Glance

| # | Notebook | Topics |
|---|----------|--------|
| 1 | `1_Strings_Tuples__assn.ipynb` | concatenation, slicing, string methods, tuple operations |
| 2 | `2_Data_Structures__List__Dictionary__Set_-_Conditional_Statements.ipynb` | lists, dictionaries, sets, `if / elif / else` |
| 3 | `3__While_Loop__For_loop_and_Function.ipynb` | `while` and `for` loops, functions, guessing game, BMI calculator |
| 4 | `python_module_assn.ipynb` | support ticket manager with text cleaning and keyword analysis |

The notebooks are meant to be read in order. Project 4 is the capstone and combines dictionaries and lists, string cleaning, loops, functions and input validation from the earlier ones.

---

## 1. Strings & Tuples

**File:** `1_Strings_Tuples__assn.ipynb`

| Section | What it covers |
|---------|----------------|
| Greeting program | takes a name with `input()` and joins strings with `+` |
| Slicing | `str3[0]`, `str3[-1]`, `str3[0:5]`, `str3[0:11]`, `str3[::-1]`, `str3[-18:-12]` on `"Hello Bharat welcome to python programming"` |
| String methods | `upper()`, `lower()`, `capitalize()`, `count('t')`, `replace()` on `"Python beginner tutorial"` |
| Tuples | concatenation, repetition (`* 3`), indexing and slicing on `(10, 20, 30)` and `(40, 50, 60)` |

**Sample output**

```text
enter your name = Bharat
Hello Bharat welcome to python programming
```

**Key takeaways**

- Strings and tuples are immutable. Methods like `replace()` return a new string.
- `count()` is case-sensitive.
- Negative indices count from the end, and `[::-1]` reverses a sequence.

---

## 2. Data Structures & Conditionals

**File:** `2_Data_Structures__List__Dictionary__Set_-_Conditional_Statements.ipynb`

**Lists:** uses `age_list` and `name_list` to practice `append`, `insert`, `remove`, `pop`, `extend` and `sort(reverse=True)`. Statistics on the age list: max `32`, min `24`, sum `252`. Also covers indexing, range slicing and reversing the name list.

**Dictionary:** `students_marks` maps five students to marks out of 100. It covers reading a value, adding a student (`Janani: 80`), updating a mark, and the `keys()`, `values()` and `items()` methods.

**Sets:** shows that duplicates are removed automatically, and that a set cannot be indexed because it is unordered. Uses `union()` and `intersection()` on `{1, 3, 5, 7, 9}` and `{2, 3, 5, 8, 10}`.

**Conditionals:** classifies a score entered by the user.

| Score | Output |
|-------|--------|
| greater than 7 | Above average |
| 4 to 7 | Average: Good effort! Keep practicing... |
| below 4 | Below Average |

**Notes**

- `keys()`, `values()`, `items()`, `union()` and `intersection()` are called without `print()`, so they show no output. Wrap them in `print()` to see results.
- The prompt allows scores from 0 to 7, so the "Above average" branch only runs for out-of-range input.
- `name_list` has four names, not five.

---

## 3. Loops & Functions

**File:** `3__While_Loop__For_loop_and_Function.ipynb`

### Number Guessing Game

The computer picks a secret number from 1 to 10 with `random.randint()`. The player gets 3 attempts.

- A correct guess prints `You Won` and exits with `break`.
- A wrong guess prints `Try Again` and uses up an attempt.
- A number above 10 shows a warning and does not use an attempt.
- Running out of attempts triggers the `while-else` block: `Attempts over, Game over`.

```text
enter the number 1
Attempt no 1/3
Try Again
enter the number 2
Attempt no 2/3
You Won
```

### Multiplication Table

Asks for a number and prints its table from 1 to 10 using a `for` loop and f-strings.

```text
Enter the number 6
6x1 = 6
6x2 = 12
...
6x10 = 60
```

### BMI Calculator

`calculate_bmi(Weight, Height)` takes weight in kg and height in feet, converts the height to meters (`ft * 0.3048`) and returns `weight / height_m²`.

```text
Enter your Weight in(kgs) 58
Enter your Height in (ft) 5.10
Your BMI= 24.0
```

**Notes**

- Height is read as decimal feet, so `5.10` means 5.10 ft, not 5 ft 10 in.
- The guessing game rejects numbers above 10 but not below 1.
- Non-numeric input raises a `ValueError`, since there is no error handling yet.

---

## 4. Support Ticket Analyzer

**File:** `python_module_assn.ipynb`

A mini project that manages customer support tickets stored as a dictionary of lists, where each index across the lists is one ticket.

```python
ticket_data = {
    'Ticket_No': [...],
    'Customer_Name': [...],
    'Issue_Description': [...],
    'Priority': [...]
}
```

### How It Works

| Step | What happens |
|------|--------------|
| 1. Load | 10 preloaded tickets are printed as a table with `print_ticket_table()` |
| 2. Add | The user adds new tickets. Numbers continue from `max(existing) + 1`, and priority must be High, Medium or Low |
| 3. Clean | `clean_text()` normalizes every issue description |
| 4. Keywords | `count_tickets_with_word()` counts `poor`, `good`, `slow` and `excellent` |
| 5. Summarize | Prints priority counts, the longest description and the unique words |

### Text Cleaning Rules

1. Remove all punctuation
2. Convert to lowercase
3. Collapse extra whitespace
4. Replace slang using `SLANG_MAP`

| Slang | Replaced with |
|-------|---------------|
| `ok` | `okay` |
| `u` | `you` |
| `plz` | `please` |
| `asap` | `as soon as possible` |
| `bad` | `poor` |

**Example:** `Plz fix my WiFi ASAP!!` becomes `please fix my wifi as soon as possible`.

**Final summary includes**

- The cleaned ticket table
- Counts of High, Medium and Low priority tickets
- The ticket with the longest description (number, customer, text, word count)
- The count and sorted list of unique words

**Limitations**

- Keyword matching is whole-word only (`slow` does not match `slowly`).
- Punctuation is removed without adding a space, so `service...quick` becomes `servicequick`.
- Negation is not handled (`not bad` becomes `not poor`).
- Data lives in memory only and is lost when the program ends.

---

## Skills Demonstrated

- String manipulation and slicing
- Lists, tuples, dictionaries and sets
- Conditional logic and input validation
- `while` loops, `for` loops, `break` and `continue`
- Writing and calling functions
- Text preprocessing and keyword frequency analysis
- Reading user input and formatting output

## Getting Started

**Prerequisites:** Python 3.x and Jupyter Notebook, JupyterLab, or VS Code with the Jupyter extension. No external libraries are needed, since only the built-in `string` and `random` modules are used.

```bash
git clone https://github.com/<your-username>/<your-repo-name>.git
cd <your-repo-name>
jupyter notebook
```

Open any notebook and run the cells in order. Several notebooks ask for input, so watch for the prompts.

## Repository Structure

```text
.
├── 1_Strings_Tuples__assn.ipynb
├── 2_Data_Structures__List__Dictionary__Set_-_Conditional_Statements.ipynb
├── 3__While_Loop__For_loop_and_Function.ipynb
├── python_module_assn.ipynb
└── README.md
```
