# EXP-06: AI-Assisted Programming and Debugging

# Date : 20.08.2026
## NAME: Akshaya Lakshmi V
## REG NO: 212224060014

---

# AIM

To use AI tools for programming and debugging tasks in Python, C, and Java, and to evaluate their ability to generate code, identify bugs, optimize programs, explain complexity, and generate unit tests.

---

# OBJECTIVE

The objective of this experiment is to understand how AI tools can assist programmers in different stages of software development, including:

- Writing programs
- Debugging errors
- Optimizing code
- Analyzing time and space complexity
- Generating unit tests
- Comparing AI-assisted programming with manual coding

---

# PROBLEM STATEMENT

Develop a simple program to check whether a given number is a **Palindrome** using Python, C, and Java.

The same programming problem is implemented in all three languages using AI assistance.

The generated programs are then:

1. Tested for correctness.
2. Analyzed for bugs.
3. Optimized.
4. Evaluated for time and space complexity.
5. Tested using automatically generated unit tests.
6. Compared with manually written code.

---

# PROCEDURE

```text
Problem Definition
       ↓
Generate Python Code
       ↓
Generate C Code
       ↓
Generate Java Code
       ↓
Identify Bugs
       ↓
Optimize Code
       ↓
Analyze Complexity
       ↓
Generate Unit Tests
       ↓
Compare Manual vs AI-Assisted Coding
       ↓
Code Quality Analysis
```

---

# 1. PYTHON PROGRAM

## Prompt Used

> Write a Python program to check whether a given number is a palindrome. Use a function, include comments, and handle negative numbers appropriately.

## AI-Generated Code

```python
def is_palindrome(number):
    if number < 0:
        return False

    original = str(number)
    return original == original[::-1]

number = 12321

if is_palindrome(number):
    print("Palindrome")
else:
    print("Not a Palindrome")
```

## Output

```text
Palindrome
```

---

# 2. C PROGRAM

## Prompt Used

> Write a C program to check whether a given integer is a palindrome using a function.

## AI-Generated Code

```c
#include <stdio.h>

int isPalindrome(int num)
{
    int original = num;
    int reverse = 0;

    while(num > 0)
    {
        reverse = reverse * 10 + num % 10;
        num /= 10;
    }

    return original == reverse;
}

int main()
{
    int number = 12321;

    if(isPalindrome(number))
        printf("Palindrome\n");
    else
        printf("Not a Palindrome\n");

    return 0;
}
```

## Output

```text
Palindrome
```

---

# 3. JAVA PROGRAM

## Prompt Used

> Write a Java program to check whether a given integer is a palindrome using a method.

## AI-Generated Code

```java
public class Palindrome {

    static boolean isPalindrome(int num)
    {
        if(num < 0)
            return false;

        int original = num;
        int reverse = 0;

        while(num > 0)
        {
            reverse = reverse * 10 + num % 10;
            num /= 10;
        }

        return original == reverse;
    }

    public static void main(String args[])
    {
        int number = 12321;

        if(isPalindrome(number))
            System.out.println("Palindrome");
        else
            System.out.println("Not a Palindrome");
    }
}
```

## Output

```text
Palindrome
```

---

# 4. BUG IDENTIFICATION

## Prompt Used

> Review the following program for logical, syntax, runtime, and edge-case bugs. Identify any problems and suggest corrections.

## Example Bug

Consider the following Python code:

```python
def is_palindrome(number):
    return str(number) == str(number)
```

### Problem

The function compares the string with itself instead of its reverse, causing every input to return **True**.

### Example

```text
Input: 123
Expected Output: False
Actual Output: True
```

### Corrected Code

```python
def is_palindrome(number):
    if number < 0:
        return False

    text = str(number)
    return text == text[::-1]
```

### Observation

Comparing the original string with its reversed version correctly identifies palindrome numbers.

---

# 5. CODE OPTIMIZATION

## Prompt Used

> Optimize the palindrome program while maintaining correctness. Explain whether the optimization improves its time or space complexity.

## Optimized Approach

The optimized version avoids string conversion and reverses the digits mathematically.

```python
def is_palindrome(num):

    if num < 0:
        return False

    original = num
    reverse = 0

    while num > 0:
        reverse = reverse * 10 + num % 10
        num //= 10

    return original == reverse
```

### Optimization Analysis

The optimized algorithm:

- Eliminates string conversion.
- Uses arithmetic operations only.
- Uses constant extra memory.
- Produces the same correct result.

---

# 6. COMPLEXITY ANALYSIS

## Prompt Used

> Explain the time and space complexity of the palindrome algorithm in Python, C, and Java.

## Time Complexity

Each digit is processed once.

```text
Time Complexity = O(d)
```

where **d** is the number of digits.

## Space Complexity

Only a few variables are used.

```text
Space Complexity = O(1)
```

### Complexity Comparison

| Language | Time Complexity | Space Complexity |
|---|---|---|
| Python | O(d) | O(1) |
| C | O(d) | O(1) |
| Java | O(d) | O(1) |

The algorithm has identical asymptotic complexity in all three programming languages.

---

# 7. UNIT TEST GENERATION

## Prompt Used

> Generate unit test cases for a palindrome function. Include normal, negative, non-palindrome, zero, and single-digit inputs.

## Test Cases

| Test Case | Input | Expected Output |
|---|---|---|
| Palindrome | 121 | True |
| Non-Palindrome | 123 | False |
| Negative Number | -121 | False |
| Zero | 0 | True |
| Single Digit | 8 | True |
| Large Palindrome | 123454321 | True |

## Python Unit Test Example

```python
import unittest

class TestPalindrome(unittest.TestCase):

    def test_palindrome(self):
        self.assertTrue(is_palindrome(121))

    def test_not_palindrome(self):
        self.assertFalse(is_palindrome(123))

    def test_negative(self):
        self.assertFalse(is_palindrome(-121))

    def test_zero(self):
        self.assertTrue(is_palindrome(0))

    def test_single_digit(self):
        self.assertTrue(is_palindrome(8))

if __name__ == "__main__":
    unittest.main()
```

---

# 8. MANUAL CODING VS AI-ASSISTED CODING

| Criteria | Manual Coding | AI-Assisted Coding |
|---|---|---|
| Development Speed | Moderate | Very Fast |
| Code Generation | Requires manual effort | Automatically generated |
| Debugging | Developer identifies errors | AI suggests fixes |
| Optimization | Requires experience | AI recommends improvements |
| Complexity Analysis | Manual effort | AI provides instant explanation |
| Unit Tests | Written manually | Automatically generated |
| Learning | Better conceptual understanding | Faster with explanations |
| Risk of Errors | Depends on programmer | AI may generate incorrect logic |
| Customization | High | Depends on prompt quality |
| Overall Productivity | Moderate | High |

---

# CODE QUALITY ANALYSIS

The AI-generated programs were evaluated using the following criteria:

- Correctness
- Readability
- Efficiency
- Maintainability
- Error Handling

| Language | Correctness | Readability | Efficiency | Error Handling | Overall |
|---|---|---|---|---|---|
| Python | Excellent | Excellent | Excellent | Very Good | Excellent |
| C | Excellent | Very Good | Excellent | Good | Very Good |
| Java | Excellent | Excellent | Excellent | Very Good | Excellent |

---

# OBSERVATION

- AI generated correct programs in Python, C, and Java.
- AI quickly identified logical bugs and suggested fixes.
- Complexity analysis and optimization were generated automatically.
- AI produced useful unit-test cases covering common and edge cases.
- Human review is still essential before deploying AI-generated code.

---

# RESULT

Python, C, and Java programs for checking whether a number is a palindrome were successfully generated using AI assistance. Bugs were identified and corrected, the algorithm was optimized, time and space complexities were analyzed, and unit tests were generated successfully.

---

# CONCLUSION

AI-assisted programming significantly improves development speed by helping programmers generate code, debug programs, optimize algorithms, analyze complexity, and generate unit tests. However, AI-generated code should always be verified through testing and manual review. The experiment demonstrates that combining **manual programming skills with AI assistance** results in a more efficient and reliable software development process.
