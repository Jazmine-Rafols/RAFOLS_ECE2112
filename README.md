# **ECE2112: Programming Assessment 1**
**Submitted by: Jazmine Mikaela L. Rafols | 2ECE-D**   
**Submitted on: August 27, 2026**
 ### **Objectives of the Experiment**
> Upon accomplishing Programming Assessment 1, the student should be able to demonstrate the utilization of basic Python functions, operators, and string operations and manipulate these strings through indexing, slicing, and built-in string methods, as well as the application of sequence unpacking to manipulate elements of a list. The use of Python functions and the given methods are used to return an instructed and expected result.
### **A. Word Rotation Problem**
---
> **Instruction:** Create a function that moves the first character of the string to the end while keeping all remaining characters in their original order and preserving the capitalization of every character. 

Upon approaching the problem, part of its solution requires a method that is able to manipulate a character in a string. In Python, there is an existing operation that allows the access to a specific element within an iterable sequence, referred to as **indexing**. 

When accessing an element in a sequence, they are defined by their index values. As Python utilizes zero-based indexing, their index values will begin from `[0]` and increase by `1` for every character, including spaces, in the sequence. As such, a program can call an element using indexing to use in a multitude of tasks. 

An example of indexing would be as followed:
```python
text = "Code"   
print(text[0]) 
```
Following the index values of this example, the list would refer to the characters of a string as `[0] = "C"`, `[1] = "o"`, `[2] = "d"`, and `[3] = "e"`, respectively. This would mean that `print(text[0])` will return the character: `C`. 

However, the problem asks to isolate the remaining characters in a string, keeping them unaffected as the first character is taken from the string. Therefore, there is another string operation that can be utilized to acquire the desired effect.

**Slicing** is an operation used to extract a range of specific items to create a new sub-sequence through using the colon `:` sign and `start:end:step` syntax. This is distinct from indexing where it can only access an individual element.

Slicing can be demonstrated as:
```python
text = "Code"  
print(text[1:])
```
As aforementioned, `[1]` would be "o" and applying the slice operation on the index value `[1]` would mean, "Every value starting from `[1]`", which is "o" until "e". The corresponding output would be: `ode`.

Considering that the operations required to execute the function are now identified, the function `rotate_word(text)` for word rotation can now be defined as:
```python
def rotate_word(text):
    new_word = text[1:] + text[0]
    return new_word
```
Under this function, the variable `new_word` will manipulate the initial variable `text` using the slice operation starting from index `[1]` to isolate the characters following the first element, then index `[0]`, the first character, will be reconnected through concatenation `+` at the end of string. Referencing from the previous two examples, if `text = "Code"`, then rotate_word(text) would return as: `odeC`.

### B. Username Builder Problem
---
> **Instruction:** Create a function that accepts two strings: first_name and last_name. The function must be able to convert all letter to lowercase, remove spaces from the first_name and last_name strings, and join the processed strings using one period. 

The function asks for the two strings, `first_name` and `last_name`, to be attached through a period `.` while having the strings converted to lowercase and have the spaces removed in between.

The method that can solve the lowercase requirement would be `lowercase()`, a built-in string method that will convert all characters of a string to lowercase while symbols and numbers are ignored, as demonstrated here:
```python
fruit = "MANGO"
print(fruit.lower())
```
This code would return `mango` as its output. Additionally, the string method `replace()` can remove the spaces between the strings. Combining these two methods together, the syntax will look as shown below:
```python
fruit.lower().replace(" ","") #fruit as an example
```
The quotation marks `" "` with the empty space signifies the space in the strings and the following marks means it will replace every space featured with `""`, essentially removing that space.

To complete the function, the period can be concatenated as so: `+ "."`, following the variable. The final function `make_username(first_name, last_name)` can now be defined as:
```python
def make_username(first_name, last_name):
    username = first_name.lower().replace(" ", "") + "." + last_name.lower().replace(" ", "")
    return username
```
### C. Bookend Swap Problem
---
> **Instruction:** Create a function named `swap_bookends()` that accepts a list containing at least two elements. This function should unpack the list into three variables: `first`, `middle`, and `last`. Using these variables, return a new list in which the first and last elements have exchanged positions while the elements in the middle must remain in their original order. 

The problem asks for the function to unpack the list into three variables, in which it can be done through the method of **extended sequence unpacking**. This method is done through the use of the asterisk `*` prefix, allowing a variable to capture or store multiple elements from an iterable sequence into a list of its own. As for this, the instructions have required the use of extended sequence unpacking in the following form: `first, *middle, last = items`.

A demonstration of extended sequence unpacking is as followed:
```python
a, *b, c = (1, 2, 3, 4)
```
The contents of `a`, `*b`, and `c` would be `a = 1`, `*b = (2, 3)`, `c = 4`, respectively. In terms of the three given variables by the problem, the elements would be allocated like this:
- `first`- assigns the beginning element into the `first` variable.
- `*middle` - stores the elements in between the first and last element.
- `last` - assigns the ending element into the `last` variable.

Furthermore, the requirement of exchanging the positions of the `first` and `last` variables can be done through rewriting their order through the `return` feature of the defined function into: `last, *middle, first`.

Utilizing this method of assigning variables allows a non-mutating function to be executed and retains the elements original placements after returning a new list. Thus, the final function `swap_bookends(items)` is as shown below:
```python
def swap_bookends(items):
    first, *middle, last = items
    return [last, *middle, first]
```
---
### Thank you for Reading!
To view the complete program for Programming Assessment 1, refer to this link: [Programming Assessment 1 by Jazmine Rafols](https://github.com/Jazmine-Rafols/RAFOLS_ECE2112/blob/8de3d6d3f74398ca4cd62fba70f4adb134ff2605/RAFOLS_Programming_Assessment-1.ipynb)
### File Version History
**August 26, 2026** - Initial README file uploaded in GitHub. \
**August 27, 2026** - File reupload. \
**August 28, 2026** - Rewritten the format of README file for better readability.
