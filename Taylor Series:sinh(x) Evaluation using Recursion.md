
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
