from functools import reduce

# 1. Default and Keyword Arguments
def greet(name, message="Welcome!"):
    print(f"Hello {name}, {message}")
greet("Alice")
greet(name="Bob", message="Good Morning!")

# 2. *args and **kwargs
def show_info(*args, **kwargs):
    print("Args:", args)
    print("Kwargs:", kwargs)
show_info(1, 2, 3, name="Tom", age=30)

# 3. Recursive Function (Factorial)
def factorial(n):
    return 1 if n == 0 else n * factorial(n - 1)
print("Factorial of 5:", factorial(5))

# 4. Lambda, map, filter, reduce
nums = [1, 2, 3, 4, 5]
print("Lambda Square:", (lambda x: x*x)(4))
print("map():", list(map(lambda x: x**2, nums)))
print("filter():", list(filter(lambda x: x % 2 == 0, nums)))
print("reduce():", reduce(lambda x, y: x * y, nums))
