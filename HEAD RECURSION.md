# 🔁 Types of Recursion: Head Recursion in Python

## 🎯 AIM:
To write a Python program to demonstrate **Head Recursion** by finding and printing the sequence based on the sum of all digits (even or odd adjusted input).

## 🧠 ALGORITHM:

1. **Start**
2. Define a recursive function `fun(n)`
3. In the function:
   - Create a recursive call at the **beginning** (Head Recursion)
   - Print the result after the recursive call
4. Take input from the user
5. If input is odd, convert it to the next even number
6. Call the recursive function
7. **Stop**

## 💻 PROGRAM:
```python
def fun(n):
    if n == 0:
        return
    fun(n - 2)   # Head recursion (recursive call first)
    print(n)


num = int(input("Enter a number: "))

if num % 2 != 0:
    num += 1

fun(num)

```

## OUTPUT
<img width="1254" height="256" alt="image" src="https://github.com/user-attachments/assets/c49e26d9-1851-4c1a-a8c8-758fd3182596" />


## RESULT
The program successfully demonstrates Head Recursion in Python. The recursive call is made at the beginning, and results are printed during the backtracking phase, generating a sequence of even numbers.
