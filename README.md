# PythonCheatSheet
A cheat sheet for Python syntax and methods. Designed to be used as a refresher - not for beginners.

## Collections

### Lists

#### Creating a List
```python
fruits = ['apple', 'banana', 'cherry']
```

#### Add a New Element at the End
```python
fruits.append('date')  # ['apple', 'banana', 'cherry', 'date']
```

#### Inserting an Element at a Specific Position
```python
fruits.insert(1, 'bilberry')  # ['apple', 'bilberry', 'banana', 'cherry', 'date']
```

#### Removing a Particular Element
```python
fruits.remove('banana')  # ['apple', 'bilberry', 'cherry', 'date']
```

#### Removing with pop
```python
fruits.pop(2)  # 'cherry', ['apple', 'bilberry', 'date']
```

#### Clearing all Elements
```python
fruits.clear()  # []
```

#### Accessing Elements Using Indexing
```python
first_fruit = fruits[0]  # 'apple'
last_fruit = fruits[-1]  # 'date'
```

#### Slicing
```python
my_list = [1, 2, 3, 4, 5]
slice_list = my_list[2:4]  # [3, 4]
```

#### Concatenation
```python
concatenate_list = my_list + [6, 7, 8]  # [1, 2, 3, 4, 5, 6, 7, 8]
```

#### Repetition
```python
repeat_list = my_list * 2  # [1, 2, 3, 4, 5, 1, 2, 3, 4, 5]
```

#### Finding the First Occurrence of an Element
```python
found_1_in_list = 1 in my_list  # True
index_1_in_list = my_list.index(1) if found_1_in_list else -1  # 0
```

#### Counting Element Occurrences
```python
count_1s = my_list.count(1)  # 1
```

#### Sorting Items in a List
```python
sorted_list = sorted(my_list, reverse=True)  # [5, 4, 3, 2, 1]
```

#### Sorting List in Place
```python
my_list.sort()
```

#### Reversing a List
```python
reversed_list = reversed(my_list)  # [5, 4, 3, 2, 1]
my_list.reverse()
```

#### Copying a List
```python
copy_list = my_list.copy()
```

#### Length of List
```python
length = len(my_list)  # 5
```

#### Minimum and Maximum of List
```python
min_element = min(my_list)  # 1
max_element = max(my_list)  # 5
```

#### Sum of List
```python
sum_of_elements = sum(my_list)  # 15
```

#### Enumerating List
```python
for index, value in enumerate(my_list):
    print(index, value)
```

#### Checking if All/Any Elements are True
```python
all_true = all(my_list)  # True if all elements are true
any_true = any(my_list)  # True if any element is true
```

### Special List Operations

#### Adding Lists
```python
merged = my_list + another_list
```

#### Creating a Boolean List
```python
visited = [False] * len(input_string)
# Check if all elements are True
all_true = all(visited)
```

## Strings

### Creating a String
```python
greeting_string = "Hello, world!"
```

### Accessing Characters Using Indexing
```python
first_char = greeting_string[0]  # 'H'
last_char = greeting_string[-1]  # '!'
```

### Slicing
```python
my_string = "Hello"
slice_string = my_string[1:3]  # "el"
```

### Concatenation
```python
concatenate_string = my_string + ", world!"  # "Hello, world!"
```

### Repetition
```python
repeat_string = my_string * 2  # "HelloHello"
```

### Case Conversions
```python
lowercase_greeting = greeting_string.lower()  # 'hello, world!'
print('mark'.upper())  # 'MARK'
print('Mark'.lower())  # 'mark'
```

### String Methods

#### `.split()`
```python
sentence = 'Python is fun!'
words = sentence.split()  # ['Python', 'is', 'fun!']

data = 'John,Doe,35,Engineer'
info = data.split(',')  # ['John', 'Doe', '35', 'Engineer']
```

#### `.join()`
```python
words = ['Programming', 'with', 'Python', 'is', 'exciting!']
sentence = ' '.join(words)  # 'Programming with Python is exciting!'
```

#### `.strip()`
```python
name = '    John Doe    \t\n'
name = name.strip()  # 'John Doe'

name = '    John Doe    '
print(name.lstrip())  # 'John Doe    '
print(name.rstrip())  # '    John Doe'
```

### Character Operations
```python
print(ord('A'))  # 65
print(chr(65))  # 'A'
print(chr(ord('A') + 1))  # 'B'
```

### Checking String Content
```python
print("C".isalpha())  # True
print("C++".isalpha())  # False
print("239".isdigit())  # True
print("C239".isdigit())  # False
print("C98".isalnum())  # True
print("C98++".isalnum())  # False
'string'.isnumeric()  # Returns True if all characters are numeric
'string'.isdigit()  # Returns True if all characters are digits
'string'.isdecimal()  # Returns True if all characters are decimal
```

### Combining Methods
```python
numbers = '1,2,3,4,5'
num_list = [int(number) for number in numbers.split(',')]  # [1, 2, 3, 4, 5]
average = sum(num_list) / len(num_list)
print('The average is', average)  # The average is 3.0
```

### Split a String into a List of Each Character
```python
word = "hello"
word_list = list(word)  # ['h', 'e', 'l', 'l', 'o']
```

## Loops

### For Loops
```python
friends = ['Alice', 'Bob', 'Charlie', 'Daniel']
for friend in friends:
    print(f"Hello, {friend}! Nice to meet you.")

for num in range(5):
    print(num)
```

### While Loops
```python
num = 0
while num < 5:
    print(num)
    num += 1
```

### Looping Over Collections

#### List
```python
fruits = ['apple', 'banana', 'cherry']
for fruit in fruits:
    print(fruit)
```

#### String
```python
word = 'hello'
for letter in word:
    print(letter)
```

### Applications of Looping

#### Summing a List of Numbers
```python
numbers = [1, 2, 3, 4, 5]
total = 0
for num in numbers:
    total += num
print(total)  # 15
```

#### Counting Vowels
```python
text = 'hello'
vowel_count = 0
for letter in text:
    if letter in 'aeiou':
        vowel_count += 1
print(vowel_count)  # 2
```

### Conditional Looping

#### The `break` Statement
```python
numbers = [1, 3, 7, 9, 12, 15]

for number in numbers:
    if number % 2 == 0:
        print("The first even number is:", number)  # Stops the loop after printing the first even number.
        break
    print("Number:", number)
```
Outputs:
```
Number: 1
Number: 3
Number: 7
Number: 9
The first even number is: 12
```

#### The `continue` Statement
```python
for i in range(6):
    if i == 3:
        continue
    print(i)
```
Outputs:
```
0
1
2
4
5
```

### Use-case with a For Loop
```python
names = ["Alice", "Bob", "Charlie", "David"]

for name in names:
    if name == "Charlie":
        print("Found Charlie!")
        break
```

## Miscellaneous

### Rounding Up Dividing `n` (used for finding middle index)
```python
int(n // 2) + int(n % 2)
```

### For Loop Range()
```python
for i in range(start, stop, step):
```

### `is` Keyword
```python
a = [1, 2, 3]
b = a
c = [1, 2, 3]

print(a is b)  # True
print(a is c)  # False
```

### Jumping from `try` to `except`
```python
try:
    # Some code
    raise Exception
except Exception:
    # Handle exception
```
