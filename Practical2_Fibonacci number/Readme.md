#Recursive Implementation
def fibonacci_recursive(n):
    """
    Function to calculate the nth Fibonacci number using recursion.
    Base cases:
        - If n is 0, return 0
        - If n is 1, return 1
    For all other cases:
        - Return the sum of the two previous Fibonacci numbers
    """
    if n == 0:
        return 0
    elif n == 1:
        return 1
    else:
        return fibonacci_recursive(n - 1) + fibonacci_recursive(n - 2)

# Example usage:
n = 6
print(f"Recursive: The {n}th Fibonacci number is {fibonacci_recursive(n)}")

#Iterative Implementation
def fibonacci_iterative(n):
    """
    Function to calculate the nth Fibonacci number using iteration (loop).
    Starts from the base values 0 and 1, and iteratively builds up to the nth value.
    """
    if n == 0:
        return 0
    elif n == 1:
        return 1
    
    a, b = 0, 1  # Initialize first two Fibonacci numbers
    for _ in range(2, n + 1):
        a, b = b, a + b  # Update a and b to next Fibonacci numbers
    return b

# Example usage:
n = 6
print(f"Iterative: The {n}th Fibonacci number is {fibonacci_iterative(n)}")