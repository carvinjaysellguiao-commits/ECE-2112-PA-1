# ECE-2112-PA-1

Made by: Carvin Jaysell D. Guiao | 2ECE-D

Python Implementations for Programming Assignment 1:


## A. Word Rotation Problem

This section handles moving the leading character of a given word to the very end of the string while preserving the capitalization and order of every character. The objective is to perform this rotation in a single step using basic Python string operations. The required Python function `rotate_word(text)` accepts a non-empty string as input, then returns a new string in which the first character is transferred to the end while preserving the order and capitalization of all remaining characters, using string indexing or slicing to construct the result.

```python
  def rotate_word(text):
    if len(text) == 1:
      return text
    return text[1:] + text[0]
```

The `rotate_word (text)` function shifts the leading character of a non-empty string to the end while keeping the remaining letters in their original sequence and capitalization. `if len(text) == 1` checks whether the string has only one character so the function can return it immediately without performing any rotation. It then achieves this in a single line using string slicing `text[1:]` to capture everything from index 1 onwards, and indexing `text[0]` to isolate the first letter. The final cell `return text[1:] + text[0]` creates a new string by taking all characters except the first `text[1:]` and then adding the first character `text[0]` at the end.

**Executing test cases**
```python
print(rotate_word("python")) #Output: "ythnop"
print(rotate_word("logic")) #Output: "ogicl"
print(rotate_word("Code")) #Output: "odeC"
print(rotate_word("A")) #Output: "A"
```

## B. Username Builder Problem

This section converts two input strings, a first name and a last name, into a clean, standardized username format. The objective is to process multiword or improperly capitalized names and combine them into a single `first.last` output suitable for system account creation. The required Python function `make_username(first_name, last_name)` takes a first name and last name as strings and produces a formatted username by converting all letters to lowercase, removing any spaces within each name, and then combining them into a single string separated by a period.


```python
  def make_username(first_name, last_name):
    first = first_name.lower().replace(" ", "")
    last = last_name.lower().replace(" ", "")
    return first + "." + last
```

The function uses `.lower()` to convert all characters in both names to lowercase and `.replace(" ", "")` to strip out any interior spaces. It then uses standard string concatenation: `first + "." + last` to join the cleaned strings with a period delimiter and return the finalized username.

**Executing test cases**
```python
make_username("Ada", "Lovelace") #Output: 'ada.lovelace'
make_username("Alan", "Turing") #Output: 'alan.turing'
make_username("Ana Maria", "De Leon") #Output: 'anamaria.deleon'
```

## C. Bookend Swap Problem

This section swaps the outer boundary elements of a given list while leaving all middle elements in their original positions. The solution builds a new list to ensure the input list remains completely untouched. The required Python function `swap_bookends(items)` accepts a list with at least two elements and returns a new list where the first and last elements are swapped while the middle elements remain unchanged, using extended sequence unpacking `(first, *middle, last = items)` without modifying the original list.

```python
def swap_bookends(items):
    first, *middle, last = items
    return [last, *middle, first]
```
The function uses extended sequence unpacking `first, *middle, last = items` to separate the list into its first item, its last item, and a list containing all intermediate elements `middle`. It then returns a new list using list concatenation `[last] + middle + [first]`, placing the last element at the front and the first element at the end. 

**Executing test cases**
```python
print(swap_bookends([1, 2, 3, 4, 5, 6])) #Output: [6, 2, 3, 4, 5, 1]
print(swap_bookends(["red", "green", "blue"])) #Output: ['blue', 'green', 'red']
print(swap_bookends([8, 3])) #Output: [3, 8]
```
Thank you for reading!

To see the main Python Programming Assignment 1, click this link [Programming Assignment 1](http://localhost:8888/files/Programming%20Assignments/Programming%20Assignment%201_GUIAO%2CCJ.ipynb?_xsrf=2%7C4430cad1%7Cb1e3fe9144e00526d33ea6b0ef1f8923%7C1786724141) and download. Open on Jupyter Notebook, then you can run each cells.

**README File Version History:**
<br>
August 25, 2026 - Initial README Output Uploaded
<br>
August 26, 2026 - Draft Update
<br>
August 27, 2026 - Finalization details and file upload
<br>
August 28, 2026 - Updated few details
