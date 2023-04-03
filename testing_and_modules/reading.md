# Testing and Modules

## Test-Driven Development (TDD) in Python
1-What are the key principles of Test-Driven Development (TDD) in Python, and how do they contribute to the overall quality of code?
Test-Driven Development is a strategy to think (and write!) tests first.
TDD we need to think about tests first. And to be ok with the possibility of the beginning to be hard sometimes

test file shoud be the same name  of module
we make tst to check if the result is the same expecting

## if __name__ == '__main__': statement in Python scripts
2- Explain the purpose of the if __name__ == '__main__': statement in Python scripts. What are some use cases for including this conditional in your code?
run the source file as the the main programs
used to execute some code only if the file was run directly and not imported

help to execute module as a secripts

## recursion in Python
3-Describe the concept of recursion in Python.
process in which a function call itself directly
used more memory becouse adds the stack with each recursion


## Python modules and packages
4- What is the difference between Python modules and packages? Explain how to create, import, and use them in your Python programs
The main difference between a module and a package in Python is that a module is a simple Python script with a .py extension file that contains collections of functions and global variables. In contrast, a package is a directory that contains a collection of modules, and this directory also contains an __init__.py file by which the interpreter interprets it as a package.
scaler_acad.py
def module_function(para):
    print("Creating a new Module: " + para)

app.py
import scaler_acad

we create a Python package with an __init__.py file that informs the Python Interpreter that the given folder is a Python Package.
To import a package, we type the following:
import math
In the above code, math is a package.
Only its immediate modules are imported when we import a package, not the sub-packages. If you try to access those, it will raise an AttributeError.