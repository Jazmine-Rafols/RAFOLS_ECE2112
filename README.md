# ECE2112-Programming_Assessment-1
**Submitted by: Jazmine Mikaela L. Rafols | 2ECE-D**   
**Submitted on: August 27, 2026**
 ### **Objectives of the Experiment**
> Upon accomplishing Programming Assessment 1, the student was able to demonstrate the utilization of basic Python functions, operators, and string operations and manipulate these strings through indexing, slicing, and built-in string methods, as well as the application of sequence unpacking to manipulate elements of a list. The use of Python functions and the given methods were used to return an instructed and expected result.
### **A. Word Rotation Problem**
---
> **Instruction:** Create a function that moves the first character of the string to the end while keeping all remaining characters in their original order and preserving the capitalization of every character. 

Given that the experiment has instructed to use a specific format for the function: `rotate_word(text)`, the following methods were used in this problem:
- `text[n]` - it is an operation, referred to as '*indexing*', used to access a specific, individual element within any sequence iterable by using the element's position or index number (n), in which python utilizes zero-based indexing.
In this problem, indexing was used to get the first character by calling `[0]`, then added at the end of the string through concatenation `+`.
An example of indexing would be as followed:
```python
text = ["python", "logic", "code", "A"]`   
print(text[0]) 
```
The output of this cell block would deliver as `python`. This is because the index values go as `0 = python`, `1 = logic`, `2 = code`, and `3 = A` in a list with 4 elements.
- `text[n:n]` - it is an operation, referred to as '*slicing*', used to extract a range of specific items to create a new sub-sequence through using start, end, and step values in the syntax, unlike indexing that can only access a single element. For this problem, only basic slicing syntax was used to isolate the string from the first character.
**Example:**   
```python
text = "python"  
print(text[1:])
```
`(Output): ython`
The function `rotate_word(text)` was created by combining these two operations that will first isolate the first character of the string from the body and concatenate the first character at the end. The final function is as shown below:
```python
def rotate_word(text):
    new_word = text[1:] + text[0]
    return new_word
```
### B. Username Builder Problem
---
> **Instruction:** Create a function that accepts two strings: first_name and last_name. The function must be able to convert all letter to lowercase, remove spaces from the first_name and last_name strings, and join the processed strings using one period. 

Given that the experiment has instructed to use a specific format for the function: `make_username(first_name, last_name)`, the following functions and methods were used in this problem:
- `.lower()` - this is a string method that returns all uppercase characters in a given string into lower case while symbols and numbers are ignored. This fulfills one of the required parameters of the function.
**Example:**  
```python
fruit = "MANGO"
print(fruit.lower())
```
`(Output): mango`
- `.replace(" ", "")` - this is a string method where it is used to replace a specified substring with a new substring in the returned string. It uses old, new, and count values in its syntax to indicate what to replace, in which in this case, is the space between the strings.
**Example:**  
```python
replace_fruit = fruit.replace("MANGO", "ORANGE")
```
`(Output): ORANGE`
Through combining these two string methods, the final function is as shown below:
```python
def make_username(first_name, last_name):
    username = first_name.lower().replace(" ", "") + "." + last_name.lower().replace(" ", "")
    return username
```
### C. Bookend Swap Problem
---
> **Instruction:** Create a function named `swap_bookends()` that accepts a list containing at least two elements. This function should unpack the list into three variables: `first`, `middle`, and `last`. Using these variables, return a new list in which the first and last elements have exchanged positions while the elements in the middle must remain in their original order. 

Given that the experiment has instructed to use a specific format for the function: `swap_bookends(items)`, the following operations were used in this problem:
- `*variable` - this is an operation referred to as '*extended unpacking*', wherein the use of the asterisk `*` prefix allows a variable to capture or store multiple elements from an iterable sequence into a list of its own. For this problem, extended unpacking was used to store elements in the middle variable, allowing the elements in between the first and the last element to remain intact into a new list.
**Example:**
```python
a, *b, c = (1, 2, 3, 4)
```
`(Output): a = 1, *b = (2, 3), c = 4` \
As required, the elements are assigned into three variables that separate the list:
- `first`- assigns the beginning element into the `first` variable.
- `*middle` - stores the elements in between the first and last element.
- `last` - assigns the ending element into the `last` variable.
Assigning variables allows a non-mutating function to be executed and retains the elements original placements after returning a new list. Thus, upon completing the required tasks, the final function is as shown below:
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
**August 27, 2026** - File reupload
