# Ten Thousand 2

## Python Scope

### concept of variable scope in Python and describe the difference between local and global scope

1- Local scope
Local scope refers to a variable declared inside a function. For example, in the code below, the variable total is only available to the code within the get_total function. Anything outside of this function will not have access to it.

`def get_total(a, b):`
 `#local variable declared inside a function`
    `total = a + b;`
    `return total`

`print(get_total(5, 2))`
 >> 7

`# Accessing variable outside of the function:`
`print(total)`
 >> NameError: name 'total' is not defined

2- Enclosing scope
Enclosing scope refers to a function inside another function or what is commonly called a nested function.

In the code below, I added a nested function called double_it to the get_total function.

As double_it is inside the scope for the get_total function it can then access the variable. However, the enclosed variable inside the double_it function cannot be accessed from inside the get_total function.


`def get_total(a, b):`
    `#enclosed variable declared inside a function`
    ` total = a + b `

    `def double_it(): `

       ` #local variable `
       ` double = total * 2 `
       `print(double)`


    `double_it() `
    `#double variable will not be accessible`
    `print(double)`

    `return total`

3-  Global scope
Global scope is when a variable is declared outside of a function. This means it can be accessed from anywhere. 

In the code below, I  added a global variable called special. This can then be accessed from both functions get_total and double_it:

`special = 5`

`def get_total(a, b):`
    `#enclosed scope variable declared inside a function`
    `total = a + b`
    `print(special)`

    `def double_it():`
        `#local variable`
        `double = total * 2`
        `print(special)`

    `double_it()`

    `return total`

4-  Built-in scope
Built-in scope refers to the reserved keywords that Python uses for its built-in functions, such as print, def, for, in, and so forth.  Functions with built-in scope can be accessed at any level.

### How do the global and nonlocal keywords work in Python, and in what situations might you use them?

In Python, the global and nonlocal keywords are used to declare variables in different scopes. Here's how they work:

1- global: When you declare a variable as global, it means that the variable is defined in the global scope, which is outside any functions or classes. This allows the variable to be accessed and modified from within any function or class in the program. For example:

`x = 5`

`def my_func():`
    `global x`
    `x = 10`
    `print(x)`

`my_func()  # prints 10`
`print(x)   # prints 10`

In this example, the global keyword is used to modify the value of x from within the function my_func. Without the global keyword, the function would create a new variable called x within its local scope, and the global x variable would remain unchanged.

2- nonlocal: When you declare a variable as nonlocal, it means that the variable is defined in the enclosing scope, which is outside the current function but inside another function or class. This allows the variable to be accessed and modified from within the current function. For example:

`
def outer_func():
    x = 5
    
    def inner_func():
        nonlocal x
        x = 10
        print(x)
    
    inner_func()  # prints 10
    print(x)      # prints 10

outer_func()
`

In this example, the nonlocal keyword is used to modify the value of x from within the inner_func, which is nested inside outer_func. Without the nonlocal keyword, the x variable within inner_func would be a new variable in its local scope, and the x variable in outer_func would remain unchanged.

You would use the global and nonlocal keywords when you need to modify variables that are defined outside the current function or class. It's important to use these keywords carefully, as they can make your code harder to understand and maintain if overused. In general, it's best to keep variables within the scope where they are needed and avoid using global or nonlocal variables unless necessary.


### In your own words, describe the purpose and importance of Big O notation in the context of algorithm analysis.

Big O notation is a way of describing the efficiency of an algorithm in terms of the size of its input. It helps us analyze how much time and space an algorithm will require as the input size increases.

The purpose of Big O notation in algorithm analysis is to provide a way to compare and evaluate different algorithms based on their efficiency. By expressing the complexity of an algorithm using Big O notation, we can determine the algorithm's scalability and identify potential performance issues before deploying it on large data sets.

For example, if we have two algorithms that solve the same problem, we can use Big O notation to compare their efficiency. If one algorithm has a lower Big O complexity than the other, it means that it will be faster and use less memory for larger input sizes. This information is critical for making informed decisions about which algorithm to use for a given problem.

Big O notation is important because it helps us optimize algorithms and improve their performance. It also helps us avoid performance bottlenecks and scalability issues when dealing with large data sets. Additionally, it is a universal notation that is widely used in computer science and software engineering, so understanding it is essential for anyone working in these fields.


### Based on the Rolling Dice Example

To simulate a dice roll using Python, we can use the random module, which provides a randint() function that generates random integers between two specified endpoints. Here's an example of simulating a dice roll:

`import random

def roll_dice():
    return random.randint(1, 6)

print(roll_dice())  # prints a random integer between 1 and 6
In this example, we define a function called roll_dice() that uses the randint() function to generate a random integer between 1 and 6, which simulates rolling a dice.

To calculate the probability of rolling a specific number (e.g., the probability of rolling a 6) over a large number of trials, we can use a loop to roll the dice multiple times and count the number of times the desired number is rolled. Here's an example:

scss
Copy code
import random

def roll_dice():
    return random.randint(1, 6)

num_trials = 10000
num_successes = 0

for i in range(num_trials):
    if roll_dice() == 6:
        num_successes += 1

print("Probability of rolling a 6:", num_successes / num_trials)
In this example, we set num_trials to the number of trials we want to simulate (in this case, 10,000) and num_successes to 0. We then use a loop to roll the dice num_trials times and check if the roll is a 6. If it is, we increment num_successes.

Finally, we calculate the probability of rolling a 6 by dividing the number of successes by the total number of trials and print the result.

This code can be adapted to calculate the probability of rolling any number between 1 and 6 by changing the if statement inside the loop to check for the desired number.


## Things I want to know more about