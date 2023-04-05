# Class 03 file in python

## the purpose of the ‘with’ statement when opening a file in Python

The with statement is a replacement for commonly used try/finally error-handling statements. A common example of using the with statement is opening a file. To open and write to a file in Python

The with statement automatically closes the file after you’ve completed writing it.
The with statement works with the open() function to open a file.

## difference between the ‘read()’ and ‘readline()’ methods for file objects in Python. 

The read method reads the entire contents of a file and returns it as a string.

 
>with open("file.txt", "r") as file:
>-    content = file.read()
>-    print(content)

Python readline()
The readline method reads a single line from a file and returns it as a string. This means that if you use readline, you can read the contents of a file line by line, which can be useful for processing large files that do not fit in memory.

 
> with open("file.txt", "r") as file:
>-    line = file.readline()
>-    while line:
>--         print(line.strip())
>--         line = file.readline()

In the above example, the while loop continues to read lines from the file until readline returns an empty string, indicating the end of the file. The strip method is used to remove the line terminator from each line.

Python readlines()
The readline method reads a single line from a file and returns it as a string, while the readlines method reads the entire contents of a file and returns it as a list of strings, where each element of the list is a single line of the file.

You can see the difference of readline() and readlines() methods from the following example:

 
> with open("file.txt") as f:
>-    line = f.readline()
>-    print(line)# Prints the first line of the file


## describe the concept of exception handling in Python.

An Exception is an error that happens during the execution of a program. Whenever there is an error, Python generates an exception that could be handled. It basically prevents the program from getting crashed.

Why use Exceptions?
Many a time, there are valid as well as invalid exceptions. Exceptions are convenient in many ways for handling errors and special conditions in a program. When you think that you have a code which can produce an error, you can use exception handling technique.


## Things I want to know more about