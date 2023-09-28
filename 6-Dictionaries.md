# Dictionaries

Dictionaries in Python are a versatile data structure that allows you to store and manipulate data as key-value pairs. 

## Table of Contents
1. What is a Dictionary?
2. Creating a Dictionary
3. Accessing Dictionary Elements
4. Modifying a Dictionary
5. Dictionary Methods

### 1. What is a Dictionary?
A dictionary is an unordered collection of data in a key-value pair format. Each key is unique, and it is associated with a value. Dictionaries are enclosed in curly braces `{}` and have the format: `key: value`.

### 2. Creating a Dictionary
You can create a dictionary by enclosing key-value pairs in curly braces `{}` or by using the `dict()` constructor.

```python
# Creating an empty dictionary
empty_dict = {}
print(empty_dict)

# Creating a dictionary with key-value pairs
my_dict = {"name": "John", "age": 30, "city": "New York"}
print(my_dict)

# Creating a dictionary using the dict() constructor
another_dict = dict(name="Alice", age=25, city="Los Angeles")
print(another_dict)
```

### 3. Accessing Dictionary Elements
You can access the values in a dictionary using square brackets `[]` with the key.

```python
# Accessing values by key
name = my_dict["name"]
print("Name:", name)

# Using the get() method to access values safely
age = my_dict.get("age")
print("Age:", age)
```

### 4. Modifying a Dictionary
Dictionaries are mutable, which means you can modify their values, add new key-value pairs, or remove existing ones.

```python
# Modifying values by key
my_dict["age"] = 31

# Adding a new key-value pair
my_dict["email"] = "john@example.com"

# Removing a key-value pair
del my_dict["city"]
```

### 5. Dictionary Methods
Here are the top 20 methods for working with dictionaries:

#### 1. `clear()`
Clears all key-value pairs from the dictionary.

```python
my_dict.clear()
print(my_dict)  # Output: {}
```

#### 2. `copy()`
Creates a shallow copy of the dictionary.

```python
copy_dict = my_dict.copy()
```

#### 3. `fromkeys(keys, value=None)`
Creates a new dictionary with the specified keys, each initialized with the given value (default is `None`).

```python
keys = ["name", "age", "email"]
default_value = "N/A"
new_dict = dict.fromkeys(keys, default_value)
```

#### 4. `get(key, default=None)`
Returns the value associated with the key, or the specified default value if the key is not found.

```python
age = my_dict.get("age", 0)  # Returns 0 if "age" is not in the dictionary
```

#### 5. `items()`
Returns a list of key-value pairs as tuples.

```python
items = my_dict.items()
for key, value in items:
    print(key, value)
```

#### 6. `keys()`
Returns a list of all keys in the dictionary.

```python
keys = my_dict.keys()
```

#### 7. `values()`
Returns a list of all values in the dictionary.

```python
values = my_dict.values()
```

#### 8. `pop(key, default=None)`
Removes the key and returns its associated value, or the default value if the key is not found.

```python
email = my_dict.pop("email", "N/A")
```

#### 9. `popitem()`
Removes and returns an arbitrary key-value pair as a tuple.

```python
key, value = my_dict.popitem()
```

#### 10. `setdefault(key, default=None)`
Returns the value associated with the key. If the key is not found, it inserts the key with the specified default value.

```python
email = my_dict.setdefault("email", "N/A")
```

#### 11. `update(iterable)`
Updates the dictionary with key-value pairs from another dictionary or iterable.

```python
other_dict = {"country": "USA", "job": "Engineer"}
my_dict.update(other_dict)
```

#### 12. `len()`
Returns the number of key-value pairs in the dictionary.

```python
num_items = len(my_dict)
```

#### 13. `clear()`
Clears all key-value pairs from the dictionary.

```python
my_dict.clear()
```

#### 14. `copy()`
Creates a shallow copy of the dictionary.

```python
copy_dict = my_dict.copy()
```

#### 15. `popitem()`
Removes and returns an arbitrary key-value pair as a tuple.

```python
key, value = my_dict.popitem()
```

#### 16. `setdefault(key, default=None)`
Returns the value associated with the key. If the key is not found, it inserts the key with the specified default value.

```python
email = my_dict.setdefault("email", "N/A")
```

#### 17. `update(iterable)`
Updates the dictionary with key-value pairs from another dictionary or iterable.

```python
other_dict = {"country": "USA", "job": "Engineer"}
my_dict.update(other_dict)
```

#### 18. `len()`
Returns the number of key-value pairs in the dictionary.

```python
num_items = len(my_dict)
```

#### 19. `keys()`
Returns a list of all keys in the dictionary.

```python
keys = my_dict.keys()
```

#### 20. `values()`
Returns a list of all values in the dictionary.

```python
values = my_dict.values()
```
