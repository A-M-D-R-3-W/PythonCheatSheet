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

#### Accessing Elements Using Indexing
```python
first_fruit = fruits[0]  # 'apple'
last_fruit = fruits[-1]  # 'date'
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

### Making the Entire String Lowercase
```python
lowercase_greeting = greeting_string.lower()  # 'hello, world!'
```

### String Methods
Strings are immutable, but you can use string methods like `.lower()`, `.upper()`, and `.strip()` to work with them effectively.

## Indexing and Common Operations

### Define a List and a String
```python
my_list = [1, 2, 3, 4, 5]
my_string = "Hello"
```

### Slicing
```python
slice_list = my_list[2:4]  # [3, 4]
slice_string = my_string[1:3]  # "el"
```

### Concatenation
```python
concatenate_list = my_list + [6, 7, 8]  # [1, 2, 3, 4, 5, 6, 7, 8]
concatenate_string = my_string + ", world!"  # "Hello, world!"
```

### Repetition
```python
repeat_list = my_list * 2  # [1, 2, 3, 4, 5, 1, 2, 3, 4, 5]
repeat_string = my_string * 2  # "HelloHello"
```

### Finding the First Occurrence of an Element
```python
found_1_in_list = 1 in my_list  # True
found_8_in_list = 8 in my_list  # False
found_in_string = 'l' in my_string.lower()  # True
index_1_in_list = my_list.index(1) if found_1_in_list else -1  # 0
index_8_in_list = my_list.index(8) if found_8_in_list else -1  # -1
index_in_string = my_string.lower().index('l') if found_in_string else -1  # 2
```

### Sorting Items in a List
```python
sorted_list = sorted(my_list, reverse=True)  # [5, 4, 3, 2, 1]
```

## Loops

### For Loops
```python
friends = ['Alice', 'Bob', 'Charlie', 'Daniel']

for friend in friends:
    print(f"Hello, {friend}! Nice to meet you.")
```
Outputs:
```
Hello, Alice! Nice to meet you.
Hello, Bob! Nice to meet you.
Hello, Charlie! Nice to meet you.
Hello, Daniel! Nice to meet you.
```

```python
for num in range(5):
    print(num)
```
Outputs:
```
0
1
2
3
4
```

### While Loops
```python
num = 0
while num < 5:
    print(num)
    num += 1
```

### Loops Over Collections

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

## Looping and Character Operations

### Looping Over Strings
```python
text = "Hello, Python!"
for char in text:
    print(char)
```
Outputs each character:
```
H
e
l
l
o
,
...
```

### String Indexing Reminder
```python
try:
    text = "Hello, Python!"
    tenth_char = text[9]
    print('The tenth character is:', tenth_char)
except IndexError as e:
    print("Char access error message:", e)
```
Outputs:
```
The tenth character is: P
```

### Character Operations
```python
print(ord('A'))  # 65
print(chr(65))  # 'A'
print(chr(ord('A') + 1))  # 'B'

print('mark'.upper())  # 'MARK'
print('Mark'.lower())  # 'mark'

print("C".isalpha())  # True
print("C++".isalpha())  # False

print("239".isdigit())  # True
print("C239".isdigit())  # False

print("C98".isalnum())  # True
print("C98++".isalnum())  # False
```

### `is` Keyword
```python
a = [1, 2, 3]
b = a
c = [1, 2, 3]

print(a is b)  # True
print(a is c)  # False
```

## Python's String Methods

### `.split()`
```python
sentence = 'Python is fun!'
words = sentence.split()  # ['Python', 'is', 'fun!']

data = 'John,Doe,35,Engineer'
info = data.split(',')  # ['John', 'Doe', '35', 'Engineer']
```

### `.join()`
```python
words = ['Programming', 'with', 'Python', 'is', 'exciting!']
sentence = ' '.join(words)
print(sentence)  # 'Programming with Python is exciting!'
```

### `.strip()`
```python
name = '    John Doe    \t\n'
name = name.strip()
print(name)  # 'John Doe'

name = '    John Doe    '
print(name.lstrip())  # 'John Doe    '
print(name.rstrip())  # '    John Doe'
```

### Split a String into a List of Each Character
```python
word = "hello"
word_list = list(word)
print(word_list)  # ['h', 'e', 'l', 'l', 'o']
```

### Combining `split()`, `join()`, `strip()`, and Type Conversions
```python
numbers = '1,2,3,4,5'
num_list = [int(number) for number in numbers.split(',')]
print(num_list)  # [1, 2, 3, 4, 5]

average = sum(num_list) / len(num_list)
print('The average is', average)  # The average is 3.0
```

## Python Arrays

### Accessing Elements
```python
numbers = []
len(numbers)
```

### Reversing a Number
```python
reversed_num = int(str(num)[::-1])
```

### Rounding Up Dividing `n`
```python
int(n/2) + int(n%2)
```

### For Loop Range Advanced
```python
for i in range(start, stop, step):
```

### Boolean Lists
You can use `all(list)` to check if all elements are true:
```python
visited = [False] * len(inputString)
```

### Sorting an Array
```python
sorted_array = sorted(array)  # Sorts in ascending order
reversed_sorted = sorted(array, reverse=True)  # Sorts in descending order
```

### Adding Arrays
```python
merged = array1 + array2
```

### Numeric String Methods
```python
'string'.isnumeric()  # Returns True if all characters are numeric
'string'.isdigit()  # Returns True if all characters are digits
'string'.isdecimal()  # Returns True if all characters are decimal
```

### Jump from `try` to `except`
```python
try:
    # Some code
    raise Exception
except Exception:
    # Handle exception
```
