# Lists 

Lists in Python are a versatile and widely used data structure that allows you to store and manipulate collections of items. Lists are ordered, mutable (changeable), and can contain elements of different data types. 

## Table of Contents
1. Creating Lists
2. Accessing List Elements
3. Modifying Lists
4. List Methods

### 1. Creating Lists
You can create lists in Python by enclosing a comma-separated sequence of elements within square brackets `[]`. Here's how you can create a list:

```python
# Creating a list of integers
my_list = [1, 2, 3, 4, 5]

# Creating a list of strings
fruits = ["apple", "banana", "cherry"]
```

### 2. Accessing List Elements
You can access individual elements in a list using indexing. Python uses 0-based indexing, which means the first element is at index 0, the second at 1, and so on.

```python
# Accessing list elements
print(my_list[0])  # Output: 1
print(fruits[1])   # Output: banana
```

### 3. Modifying Lists
Lists are mutable, which means you can change their content. You can assign new values to specific elements or use list methods to modify them.

```python
# Modifying list elements
fruits[0] = "orange"
print(fruits)  # Output: ["orange", "banana", "cherry"]
```

### 4. List Methods
Now, let's explore the top 20 list methods in Python, along with examples:

#### Method 1: `append()`
Adds an element to the end of the list.

```python
fruits.append("grape")
print(fruits)  # Output: ["orange", "banana", "cherry", "grape"]
```

#### Method 2: `extend()`
Adds the elements of one list to another.

```python
more_fruits = ["mango", "strawberry"]
fruits.extend(more_fruits)
print(fruits)  # Output: ["orange", "banana", "cherry", "grape", "mango", "strawberry"]
```

#### Method 3: `insert()`
Inserts an element at a specific index.

```python
fruits.insert(1, "kiwi")
print(fruits)  # Output: ["orange", "kiwi", "banana", "cherry", "grape", "mango", "strawberry"]
```

#### Method 4: `remove()`
Removes the first occurrence of a specified element.

```python
fruits.remove("banana")
print(fruits)  # Output: ["orange", "kiwi", "cherry", "grape", "mango", "strawberry"]
```

#### Method 5: `pop()`
Removes and returns the element at a specified index. If no index is provided, it removes and returns the last element.

```python
popped = fruits.pop(2)
print(popped)  # Output: "cherry"
print(fruits)  # Output: ["orange", "kiwi", "grape", "mango", "strawberry"]
```

#### Method 6: `index()`
Returns the index of the first occurrence of a specified element.

```python
index = fruits.index("mango")
print(index)  # Output: 3
```

#### Method 7: `count()`
Returns the number of times a specified element appears in the list.

```python
count = fruits.count("kiwi")
print(count)  # Output: 1
```

#### Method 8: `sort()`
Sorts the list in ascending order.

```python
numbers = [4, 2, 7, 1, 9]
numbers.sort()
print(numbers)  # Output: [1, 2, 4, 7, 9]
```

#### Method 9: `reverse()`
Reverses the order of elements in the list.

```python
numbers.reverse()
print(numbers)  # Output: [9, 7, 4, 2, 1]
```

#### Method 10: `copy()`
Creates a shallow copy of the list.

```python
copy_of_fruits = fruits.copy()
print(copy_of_fruits)
```

#### Method 11: `clear()`
Removes all elements from the list.

```python
numbers.clear()
print(numbers)  # Output: []
```

#### Method 12: `len()`
Returns the number of elements in the list.

```python
length = len(fruits)
print(length)  # Output: 5
```

#### Method 13: `min()` and `max()`
Returns the minimum and maximum elements in the list.

```python
min_num = min(numbers)
max_num = max(numbers)
print(min_num)  # Output: 1
print(max_num)  # Output: 9
```

#### Method 14: `sum()`
Returns the sum of all elements in the list (for numeric lists).

```python
total = sum(numbers)
print(total)  # Output: 23
```

#### Method 15: `join()`
Concatenates list elements into a string using a specified separator.

```python
separator = ", "
fruits_string = separator.join(fruits)
print(fruits_string)  # Output: "orange, kiwi, grape, mango, strawberry"
```

#### Method 16: `clear()`
Removes all elements from the list.

```python
fruits.clear()
print(fruits)  # Output: []
```

#### Method 17: `copy()`
Creates a shallow copy of the list.

```python
copy_of_fruits = fruits.copy()
print(copy_of_fruits)
```

#### Method 18: `extend()`
Adds the elements of one list to another.

```python
more_fruits = ["mango", "strawberry"]
fruits.extend(more_fruits)
print(fruits)
```

#### Method 19: `insert()`
Inserts an element at a specific index.

```python
fruits.insert(1, "kiwi")
print(fruits)
```

#### Method 20: `sort()`
Sorts the list in ascending order.

```python
numbers = [4, 2, 7, 1, 9]
numbers.sort()
print(numbers)
```
