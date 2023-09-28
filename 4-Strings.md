# Strings

Strings are one of the most fundamental data types in Python. They are used to store and manipulate text data.

## Table of Contents

1. **Introduction to Strings**
2. **String Creation**
3. **Accessing Characters in a String**
4. **String Length**
5. **String Concatenation**
6. **String Slicing**
7. **String Formatting**
8. **String Methods**
   - `upper()`
   - `lower()`
   - `capitalize()`
   - `title()`
   - `swapcase()`
   - `count()`
   - `find()`
   - `replace()`
   - `strip()`
   - `lstrip()`
   - `rstrip()`
   - `startswith()`
   - `endswith()`
   - `join()`
   - `split()`
   - `isalpha()`
   - `isdigit()`
   - `isalnum()`
   - `isspace()`
   - `isupper()` and `islower()`

Let's dive into each of these topics step by step.

---

### 1. Introduction to Strings

A string in Python is a sequence of characters enclosed in single (' '), double (" "), or triple (''' ''' or """ """) quotes. Here's a simple example:

```python
my_string = "Hello, Python!"
```

### 2. String Creation

You can create strings using single, double, or triple quotes. Triple quotes are useful for multi-line strings.

```python
single_quoted = 'Single quotes'
double_quoted = "Double quotes"
multi_line = '''This is
a multi-line
string.'''
```

### 3. Accessing Characters in a String

You can access individual characters in a string using indexing. Python uses zero-based indexing, meaning the first character is at index 0.

```python
my_string = "Hello, Python!"
char = my_string[0]  # Access the first character 'H'
```

### 4. String Length

You can find the length of a string using the `len()` function.

```python
my_string = "Hello, Python!"
length = len(my_string)  # Returns 13
```

### 5. String Concatenation

You can concatenate strings using the `+` operator.

```python
str1 = "Hello"
str2 = " World"
result = str1 + str2  # Concatenates "Hello" and " World"
```

### 6. String Slicing

String slicing allows you to extract a portion of a string.

```python
my_string = "Hello, Python!"
substring = my_string[7:13]  # Extracts "Python!"
```

### 7. String Formatting

You can format strings using the `%` operator or f-strings (available in Python 3.6 and later).

```python
name = "Alice"
age = 30
formatted_string = "My name is %s and I am %d years old." % (name, age)
# OR
formatted_string = f"My name is {name} and I am {age} years old."
```

### 8. String Methods

#### `upper()`
Converts all characters to uppercase.

```python
my_string = "Hello, Python!"
result = my_string.upper()  # "HELLO, PYTHON!"
```

#### `lower()`
Converts all characters to lowercase.

```python
my_string = "Hello, Python!"
result = my_string.lower()  # "hello, python!"
```

#### `capitalize()`
Capitalizes the first character of the string.

```python
my_string = "hello, python!"
result = my_string.capitalize()  # "Hello, python!"
```

#### `title()`
Capitalizes the first character of each word in the string.

```python
my_string = "hello, python!"
result = my_string.title()  # "Hello, Python!"
```

#### `swapcase()`
Swaps the case of each character in the string.

```python
my_string = "Hello, Python!"
result = my_string.swapcase()  # "hELLO, pYTHON!"
```

#### `count()`
Counts the occurrences of a substring in the string.

```python
my_string = "Hello, Python!"
count = my_string.count("l")  # Returns 2
```

#### `find()`
Finds the first occurrence of a substring in the string and returns its index. Returns -1 if not found.

```python
my_string = "Hello, Python!"
index = my_string.find("Python")  # Returns 7
```

#### `replace()`
Replaces a substring with another substring.

```python
my_string = "Hello, Python!"
new_string = my_string.replace("Python", "World")  # "Hello, World!"
```

#### `strip()`
Removes leading and trailing whitespace characters from the string.

```python
my_string = "   Hello, Python!   "
cleaned_string = my_string.strip()  # "Hello, Python!"
```

#### `lstrip()`
Removes leading whitespace characters from the string.

```python
my_string = "   Hello, Python!   "
cleaned_string = my_string.lstrip()  # "Hello, Python!   "
```

#### `rstrip()`
Removes trailing whitespace characters from the string.

```python
my_string = "   Hello, Python!   "
cleaned_string = my_string.rstrip()  # "   Hello, Python!"
```

#### `startswith()`
Checks if the string starts with a specified prefix.

```python
my_string = "Hello, Python!"
result = my_string.startswith("Hello")  # True
```

#### `endswith()`
Checks if the string ends with a specified suffix.

```python
my_string = "Hello, Python!"
result = my_string.endswith("Python!")  # True
```

#### `join()`
Concatenates elements of an iterable using the string as a separator.

```python
my_list = ["apple", "banana", "cherry"]
result = ", ".join(my_list)  # "apple, banana, cherry"
```

#### `split()`
Splits the string into a list of substrings using a delimiter.

```python
my_string = "apple, banana, cherry"
result = my_string.split(", ")  # ["apple", "banana", "cherry"]
```

#### `isalpha()`
Checks if all characters in the string are alphabetic.

```python
my_string = "HelloPython"
result = my_string.isalpha()  # True
```

#### `isdigit()`
Checks if all characters in the string are digits.

```python
my_string = "12345"
result = my_string.isdigit()  # True
```

#### `isalnum()`
Checks if all characters in the string are alphanumeric.

```python
my_string = "Hello123"
result = my_string.isalnum()  # True
```

#### `isspace()`
Checks if all characters in the string are whitespace.

```python
my_string = "    "
result = my_string.isspace()  # True
```

#### `isupper()` and `islower()`

These methods check if all characters in the string are uppercase or lowercase, respectively.

```python
my_string = "HELLO"
result_upper = my_string.isupper()  # True
result_lower = my_string.islower()  # False
```
