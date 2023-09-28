Exercise 1: Fibonacci Sequence

Write a Python function that generates the Fibonacci sequence up to a specified limit 'n' using a loop. The Fibonacci sequence starts with 0 and 1, and each subsequent number is the sum of the previous two.

```python
def fibonacci_sequence(n):
    fib_sequence = []
    a, b = 0, 1
    while a < n:
        fib_sequence.append(a)
        a, b = b, a + b
    return fib_sequence

limit = 50
result = fibonacci_sequence(limit)
print(result)
```

Exercise 2: Prime Number Checker

Write a Python function that checks whether a given number 'n' is prime or not. A prime number is a positive integer greater than 1 that has no positive integer divisors other than 1 and itself.

```python
def is_prime(n):
    if n <= 1:
        return False
    for i in range(2, int(n**0.5) + 1):
        if n % i == 0:
            return False
    return True

number = 17  # Replace with the number you want to check
if is_prime(number):
    print(f"{number} is a prime number.")
else:
    print(f"{number} is not a prime number.")
```

Exercise 3: Palindrome Checker

Write a Python function that checks whether a given string is a palindrome. A palindrome is a word, phrase, number, or other sequence of characters that reads the same forward and backward (ignoring spaces, punctuation, and capitalization).

```python
def is_palindrome(s):
    s = s.lower().replace(" ", "").replace(",", "").replace(".", "")
    return s == s[::-1]

word = "Racecar"  # Replace with the word or phrase you want to check
if is_palindrome(word):
    print(f"'{word}' is a palindrome.")
else:
    print(f"'{word}' is not a palindrome.")
```

Exercise 4: Factorial Calculator

Write a Python function that calculates the factorial of a given non-negative integer 'n' using a loop. The factorial of a number is the product of all positive integers from 1 to 'n'.

```python
def factorial(n):
    result = 1
    for i in range(1, n + 1):
        result *= i
    return result

number = 5  # Replace with the number for which you want to calculate the factorial
print(f"The factorial of {number} is {factorial(number)}.")
```

Exercise 5: Sum of Digits

Write a Python function that calculates the sum of the digits of a positive integer 'n' using a loop.

```python
def sum_of_digits(n):
    total = 0
    while n > 0:
        total += n % 10
        n //= 10
    return total

number = 12345  # Replace with the number for which you want to calculate the sum of digits
print(f"The sum of digits in {number} is {sum_of_digits(number)}.")
```
