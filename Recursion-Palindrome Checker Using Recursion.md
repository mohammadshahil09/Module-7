# 🔁 Recursion:Palindrome Checker Using Recursion in Python

## 🎯 AIM:
To write a Python program to check whether a given string is a **palindrome** using **recursion**.

---

## 🧠 ALGORITHM:

1. **Start**
2. Define a recursive function `is_palindrome(word)`
   - **Base Case:** If the string length is less than 1, return `True`
   - **Recursive Case:** If the first and last characters match, call the function recursively on the substring without first and last characters
   - Else, return `False`
3. Get input from the user
4. Call the recursive function
5. Print whether the string is a palindrome
6. **Stop**

---

## 💻 PROGRAM:
```python
def is_palindrome(word):
    # Base case
    if len(word) < 1:
        return True
    # Recursive case
    if word[0] == word[-1]:
        return is_palindrome(word[1:-1])
    else:
        return False


string = input("Enter a string: ")


if is_palindrome(string.lower()):
    print("The string is a palindrome")
else:
    print("The string is not a palindrome")
```
## OUTPUT
<img width="356" height="166" alt="image" src="https://github.com/user-attachments/assets/ef975f79-7672-4d3f-b99f-2364fdcfeb64" />

## RESULT
The program successfully checks whether a given string is a palindrome using recursion.
