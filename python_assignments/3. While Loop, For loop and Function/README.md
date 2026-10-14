# Python Basics: Loops & Functions

![Python](https://img.shields.io/badge/Python-3.x-blue?logo=python&logoColor=white)
![Jupyter](https://img.shields.io/badge/Jupyter-Notebook-orange?logo=jupyter&logoColor=white)

A practice notebook (`3__While_Loop__For_loop_and_Function.ipynb`) with three small programs that use `while` loops, `for` loops and user-defined functions.

## Programs

| # | Program | Concepts |
|---|---------|----------|
| 1 | Number Guessing Game | `while` loop, `random`, `break`, `continue`, `while-else`, input validation |
| 2 | Multiplication Table | `for` loop, `range()`, f-strings |
| 3 | BMI Calculator | functions, `return`, unit conversion, `round()` |

## 1. Number Guessing Game

The computer picks a secret number from 1 to 10 using `random.randint()`. The player has **3 attempts** to guess it.

- A correct guess prints `You Won` and exits the loop with `break`.
- A wrong guess prints `Try Again`, increases the attempt count and continues.
- If the number is greater than 10, a warning is shown and the attempt is **not** used up.
- If all attempts are used, the `while-else` block prints `Attempts over, Game over`.

```text
enter the number 1
Attempt no 1/3
Try Again
enter the number 2
Attempt no 2/3
You Won
```

## 2. Multiplication Table

Asks for a number and prints its table from 1 to 10.

```text
Enter the number 6
6x1 = 6
6x2 = 12
...
6x10 = 60
```

## 3. BMI Calculator

`calculate_bmi(Weight, Height)` takes weight in **kg** and height in **feet**, converts the height to meters (`ft * 0.3048`) and returns:

```text
BMI = weight / (height in meters)^2
```

```text
Enter your Weight in(kgs) 58
Enter your Height in (ft) 5.10
Your BMI= 24.0
```

## Notes

- Height is read as decimal feet, so `5.10` means 5.10 ft and not 5 ft 10 in. For 5 ft 10 in, enter `5.83`.
- The guessing game only rejects numbers above 10. A value below 1 is treated as a normal (wrong) guess.
- Entering non-numeric text will raise a `ValueError`, since there is no error handling yet.

## How to Run

```bash
jupyter notebook 3__While_Loop__For_loop_and_Function.ipynb
```

Run each cell in order. Each program asks for input in the notebook.

## Requirements

Python 3.x and Jupyter Notebook. Only the built-in `random` module is used.
