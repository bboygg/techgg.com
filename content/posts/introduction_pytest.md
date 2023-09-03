---
title: "Introduction to pytest"
date: 2023-09-03T16:17:17+09:00
draft: False
---
## Introduction
This blog post aims to provide a comprehensive introduction to `pytest`, one of the most popular testing frameworks in Python. We'll explore what `pytest` is, how to install it, a simple example to kick things off, and finally, how to organize your test code.


## what is pytest? 
`pytest` is a testing framework in Python that allows for simple unit tests as well as complex functional testing. It is a feature-rich, plugin-based ecosystem for testing your Python code.

Official Documentation: [pytest](https://docs.pytest.org/en/7.1.x/getting-started.html)


## Installation

Installing `pytest` is as simple as running the following command:

```python
pip install pytest
```

## Example Code
Here is a basic example where we test a function to square a number.

First, the main code in a file called `calculator.py`:

```python
def square(n):
    return n * n
```

And here's how you can test it using pytest in a file called `test_calculator.py`:
```python
import pytest
from calculator import square

def test_positive():
    assert square(2) == 4
    assert square(3) == 9

def test_negative():
    assert square(-2) == 4
    assert square(-3) == 9

def test_zero():
    assert square(0) == 0

def test_type_error_with_str():
    with pytest.raises(TypeError):
        square('2')
```

Run the tests by using the following command:

```python
pytest test_calculator.py
```

## Organizing Your Test Code

In a larger project, you may have multiple test files. Organizing these test files is crucial for better code maintainability. One common way is to place all test files within a single directory. This is where Python packages and `__init__.py` come in handy.

### Directory Structure
An example directory structure could be:
```python
my_project/
|-- my_module/
|   |-- calculator.py
|-- tests/
|   |-- __init__.py
|   |-- test_calculator.py
```

### What is `__init__.py`?
The `__init__.py` file makes a directory into a Python package. This allows pytest to discover all test modules within this directory.

Place an empty `__init__.py` file in your tests directory:

```python
touch tests/__init__.py
```
By doing this, pytest will recognize that `tests` is a package and will search it for any test modules or test cases to execute.

And that's it! You now have a basic understanding of pytest, complete with an example and tips on how to organize your test code. 

Happy testing! 
