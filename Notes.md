# Class Notes: Working with Numbers
(Repository: _02-basics-04-numbers_)

Introduction to the basics of working with numbers in C++.

## Basic Operations
As was mentioned in previous notes, there are two basic types of numbers in C++: i) integers and ii) decimal numbers (floats).
Basic math operations can be performed on both of these types.

### Number as Constants
Numbers can be used as constants, which means we can write some simple code to print out numbers.
```cpp
cout << -56 << endl;
cout << 11.63 << endl;
```

### Simple Arithmetic
Basic arithmetic operations, add (`+`), subtract (`-`), multiply (`*`) and divide (`/`),
can be programmed directly:
```cpp
cout << 4 + 12 << endl;
cout << 36/12 << endl;
```

## Integer Truncation
C++ is very strict with data types: once a variable or constant has been declared (explicitly or implicitly as a certain type), it cannot be changed during program execution. This means that when we do integer operations, such as
```cpp
cout << 12/5 << endl;
```
we get an integer result: `2` not `2.4`.

When a decimal number (such as `2.4`) has to be converted to an integer, all the numbers after the decimal place are removed so that only the integer part remains (`2`). This is known as __truncation__. It is important to note that this is very different than __rounding__ a decimal number to the nearest integer. For example,

$$11/6=1.8333\dots$$ 

would be _truncated_ to `1`, not rounded up to `2`.

## The Modulus (%) Operator
The modulus operator (`%`) in C++ computes the __remainder__ of the division between two integers. It is formally defined as:
```cpp
a % b
```
where
- `a` is the dividend (the number being divided).
- `b` is the divisor (the number dividing `a`).

Note:
- The sign of the result follows the sign of the dividend (`a`).
- If `b == 0`, the behavior is undefined (division by zero).

#### CHALLENGE: Mathematical Definition
For integers `a` and `b`, the modulus operation is defined as:
```cpp
a % b = a - (b * (a / b))
```
where `/` is __integer division__ (_truncates_ towards zero). This explains why

$$-12 \thinspace \\% \thinspace 5 = -2$$

but 

$$-13 \thinspace \\% \thinspace 5 = -3$$

## Order of Operations
C++ obeys the __PEMDAS__ rule for order of operations: Parentheses, (Exponents), Multiplication/Division, Addition/Subtraction,
including the left to right __precedence__.
```cpp
4 + 5 * 10 = 4 + (5 * 10) = 54
```
To perform the `4+5` addition first, parentheses are reqired:
```cpp
(4 + 5) * 10 = 90
```

## Increment and Decrement Operators
Incrementing or decrementing by `1` is a common operation in programming (re: counting by one). The long way to do this in C++ is:
```cpp
i = i + 1;
i = i - 1;
```
The more efficient approach is to use the increment (`++`) and decrement (`--`) _unary_ operators:
```cpp
++i;
--i;
```
It is important to distinguish between __pre-increment__ versus __post-increment__. The following code explains the difference:
```cpp
int n = 5;

int pre = ++n;  // n is incremented first, then assigned to pre
cout << "Pre-increment: " << pre << ", n: " << n << endl;  // 6, 6

int post = n++;  // n is assigned to post first, then incremented
cout << "Post-increment: " << post << ", n: " << n << endl;  // 6, 7
```
__Aside__: The unary increment operator is how C++ got its name: the C++ programming language came after the C programming language
(which came after the B programming language). The C language introduced the `++` operator, hence C++.

C++ also has the binary increment (`+=`) and decrement (`-=`) operators for incrementing/decrementing by more than `1`:
```cpp
i += 10; // same as: i = i + 10
i -= 10; // same as: i = i - 10
```
