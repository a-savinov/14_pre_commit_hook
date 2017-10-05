# Quadratic Equations Solver

**pre-commit** script allows to run tests before the commit
 
# Installation

Please copy **pre-commit** file to _**./git/hooks**_ folder

## Ouput example

### Check commit fail:

```bash
 git commit -m "Add pre-commit hook - run unit tests before commit"

======================================================================
ERROR: test_returns_none_for_complex_solution (__main__.QuadraticEquationTestCas                                                                    e)
----------------------------------------------------------------------
Traceback (most recent call last):
  File "tests.py", line 22, in test_returns_none_for_complex_solution
    root1, root2 = get_roots(1, 2, 3)
  File "D:\devman\14_pre_commit_hook\quadratic_equation.py", line 6, in                                                                     get_roots
    root1 = (-b - sqrt(discriminant)) / (2 * a)
ValueError: math domain error

----------------------------------------------------------------------
Ran 4 tests in 0.001s

FAILED (errors=1)
Tests failed, aborting the commit
```

### Check commit pass:

```bash
$ git commit -m "Add pre-commit hook - run unit tests before commit"
....
----------------------------------------------------------------------
Ran 4 tests in 0.000s

OK
All tests passed, commiting your changes
[master 284a203] Add pre-commit hook - run unit tests before commit
 3 files changed, 38 insertions(+), 3 deletions(-)
 create mode 100644 pre-commit

```

# Project Goals

The code is written for educational purposes. Training course for web-developers - [DEVMAN.org](https://devman.org)
