# TP-01 — Python Foundations Through a Student Grade Manager

## 1. Objective

The goal of this practice is to review basic Python programming and write code that is easy to read and maintain. The example project is a **Student Grade Manager**.

This document is an original learning write-up based on a sample repository. It should be checked against the teacher's official TP instructions before submission.

## 2. Variables and constants

A **variable** stores a value that the program uses later. For example:

```python
student_name = "Dara"
scores = [80, 92, 75]
```

A **constant** is a value intended to stay the same. Python does not enforce constants, but uppercase names communicate this intention:

```python
PASSING_SCORE = 50
```

## 3. Functions

A function groups instructions that perform one task and can be reused. In `grade_utils.py`, `calculate_average()` calculates the mean of a list of scores, while `get_result()` decides whether the student passes.

```python
def calculate_average(scores):
    if not scores:
        return 0.0
    return sum(scores) / len(scores)
```

Using a function avoids repeating the same calculation in different parts of a program.

## 4. Classes, objects, and methods

A **class** describes the information and behavior an object has. The `Student` class stores a student's name and scores.

An **object** is one instance of a class. For example:

```python
student = Student("Dara", [80, 92, 75])
```

A **method** is a function defined inside a class. `average()` is a method that asks the helper function to calculate the student's average.

## 5. Modules and packages

A **module** is a Python file. This project has two modules:

- `student_grade_manager.py`
- `grade_utils.py`

The main file imports helper functions from `grade_utils.py`. This separates calculations from the program's main display logic and makes the code easier to maintain.

A **package** is a directory used to organize related modules. This small project does not need a package because two files are enough for the example.

## 6. Clean code and PEP 8

The project follows common Python style conventions:

- Use descriptive names such as `student_name` and `calculate_average`.
- Use `snake_case` for variables and functions.
- Use `PascalCase` for class names, such as `Student`.
- Use uppercase for constants, such as `PASSING_SCORE`.
- Indent code blocks with four spaces.
- Put spaces around operators and after commas.
- Keep each function focused on one task.
- Add docstrings where they help explain purpose.
- Avoid repeating grade-calculation logic.

## 7. Input validation and error handling

The helper function checks whether each score is between 0 and 100. Invalid values raise a `ValueError` with a clear message. This prevents impossible scores from being used in the report.

## 8. How to test the project

Run the program:

```bash
python student_grade_manager.py
```

Expected sample report:

```text
Student Grade Manager
---------------------
Student: Dara
Scores: 80, 92, 75
Average: 82.33
Result: Pass
```

You can also test different scores by changing the sample data near the bottom of `student_grade_manager.py`. Try scores below 50 and scores near 100.

## 9. What I learned

This example demonstrates how variables store data, constants communicate fixed values, functions reuse logic, and classes combine related data with behavior. Separating helper functions into a module also makes a project easier to understand and update. Clear names, consistent indentation, and simple error handling help make Python programs more reliable.

## 10. Final note

This is a practice example, not confirmation of the teacher's exact requirements. Before submitting, compare the file with the official TP instructions and make any required changes.
