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

# # 🔁 Recursion:Sum of Digits using Recursion in Python

## 🎯 AIM:
To write a Python program to calculate the **sum of all digits** in a number using **recursion**.

## 🧠 ALGORITHM:

1. **Start**
2. Define a recursive function `sum_digit(n)` that:
   - Returns 0 if `n <= 0` (Base Case)
   - Else, returns `n % 10 + sum_digit(n // 10)` (Recursive Case)
3. Take integer input from the user.
4. Call the recursive function and store the result.
5. Print the result.
6. **Stop**

## 💻 PROGRAM:
```python
def sum_digit(n):
   
    if n == 0:
        return 0
    # Recursive Case
    return (n % 10) + sum_digit(n // 10)


num = int(input("Enter a number: "))

result = sum_digit(num)

print("Sum of digits:", result)

```
## OUTPUT
<img width="467" height="220" alt="Screenshot 2025-09-08 085403" src="https://github.com/user-attachments/assets/6966fc70-cf5d-4722-8f75-20cf7a6682cb" />


## RESULT
The program successfully calculates the sum of digits of a number using recursion in Python.

# 📐 Taylor Series Using Recursion in Python

## 🎯 AIM:
To write a Python program to evaluate a **Taylor Series** using **recursion**, where values of `x` and `n` are taken from the user.

## 🧠 ALGORITHM:

1. **Start**
2. Create variables `x` and `n`
3. Get values for `x` and `n` from the user
4. Define a recursive function `series(x, n)`
   - **Base case:** If `n == 0`, return 1
   - **Recursive case:** Return `x**n / n + series(x, n-1)`
5. Print the result
6. **Stop**

## 💻 PROGRAM:
```python
def taylor_series(x, n):
    if n == 0:
        return 1
    return (x**n) / n + taylor_series(x, n-1)

x = float(input("Enter value of x: "))
n = int(input("Enter number of terms n: "))

result = taylor_series(x, n)
print("Taylor series sum:", result)
```

## OUTPUT
<img width="390" height="230" alt="image" src="https://github.com/user-attachments/assets/47cda7a1-6e33-4a39-be6f-1f9f2d152683" />

## RESULT
The program successfully evaluates a Taylor Series using recursion in Python.

# 📐 Taylor Series:sinh(x) Evaluation using Recursion in Python

## 🎯 AIM:
To write a Python program to evaluate the value of **sinh(x)** for **n terms** using recursion.

---

## 🧠 ALGORITHM:

1. **Start**
2. Read input for variable `x` (angle or number)
3. Read input for variable `n` (number of terms)
4. Define a function `fact(n)`:
   - If `n <= 1`, return 1
   - Else, return `n * fact(n - 1)` (recursive factorial)
5. Define a function `sinh(x, n)`:
   - If `n == 0`, return `x`
   - Else, return `(pow(x, 2*n + 1) / fact(2*n + 1)) + sinh(x, n - 1)`
6. Call the `sinh(x, n)` function and print the result
7. **Stop**

---

## 💻 PROGRAM:
```python
def fact(n):
    if n <= 1:
        return 1
    return n * fact(n - 1)

def sinh(x, n):
    if n == 0:
        return x
    return (x**(2*n + 1) / fact(2*n + 1)) + sinh(x, n - 1)


x = float(input("Enter value of x: "))
n = int(input("Enter number of terms n: "))


result = sinh(x, n)
print("sinh(x) approximation:", result)

```
## OUTPUT
<img width="550" height="225" alt="image" src="https://github.com/user-attachments/assets/eb2d8220-487d-4752-9657-c21830280ea6" />

## RESULT

The program successfully calculates sinh(x) using recursion by implementing the series expansion with factorial recursion in Python.



