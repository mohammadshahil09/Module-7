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
