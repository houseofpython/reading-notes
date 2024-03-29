
# List Comprehensions

List comprehension is a powerful and concise method for creating lists in Python that becomes essential the more you work with lists, and lists of lists.


new_list = [expression for item in iterable if condition]

new_list is the new list that will be created by the comprehension.
expression is the expression that will be evaluated for each item in the iterable.
item is the variable that takes on each value in the iterable.
iterable is a sequence, such as a list or a range, that the loop will iterate over.
condition (optional) is a boolean expression that is evaluated for each item. If it is true, the item is included in the new list. If it is false, the item is skipped.

Example : Creating a list with list comprehensions

construct a basic list using range() and list comprehensions
syntax
[ expression for item in list ]
digits = [x for x in range(10)]

print(digits)
Output

[0, 1, 2, 3, 4, 5, 6, 7, 8, 9]

# Decorator 

A decorator is a special type of function that can be used to modify or extend the behavior of another function without changing its source code. Decorators are often used to add extra functionality to existing functions, such as logging, timing, or caching.

Example 2: 

def log_function(func):
    def wrapper(*args, **kwargs):
        print(f"Calling function {func.__name__}")
        result = func(*args, **kwargs)
        print(f"Finished calling function {func.__name__}")
        return result
    return wrapper

@log_function
def add_numbers(a, b):
    return a + b
