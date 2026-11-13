# Assignment: C++ Working with Numbers
An introduction to numerical operations and functions.

### 0. Get Started
You will always do these two steps:
1. Launch Xcode and clone this repository.
2. Update the comment header with your name/date.

### 1. Basic Operations
#### Preliminary Note
As was mentioned in previous notes, there are two basic types of numbers in C++: i) integers and ii) decimal numbers (floats). 
Numbers can be used as constants, which means we can write some simple code to print out numbers.

#### Steps
Copy, paste and run the following code:
```
cout << 40 << endl;
cout << -40 << endl;
cout << 40.1234 << endl;
```
In C++, we can do some basic integer operations directly in the code itself. Copy, add and run the following code:
```
cout << 12 + 4 << endl;
cout << 12 - 4 << endl;
cout << 12 * 4 << endl;
cout << 12 / 4 << endl;
```
Now, let's repeat the above by changing the order of the numbers:
```
cout << 4 + 12 << endl;
cout << 4 - 12 << endl;
cout << 4 * 12 << endl;
cout << 4 / 12 << endl;
```

$$\large{{\text{\color{red}In Desmos, respond to Prompt 1 on Screen 2}}}$$

__\*\*Commit/Push to GitHub\*\*__ with commit message that matches the section heading: _1. Basic Operations_.

### 2. Integer _Truncation_
C++ is very strict with data types: once a variable or constant has been declared (explicitly or implicitly as a certain type), it cannot be changed during program execution. This means that when we do integer operations, such as
```
     cout << 12 / 5
```
we get an integer result (in this example, `2`).

#### Steps

In your program, add the following above `#include <iostream>`
```
#include <iomanip>
```
Before `return 0;` add the following to your program (don't worry about the code means).
```
int i;
cout << fixed << setprecision(6) << '\n';
for (i = 1; i < 22; i++) {
    cout << "21/" << i
         << "\t=\t" << 21 / i
         << "\t\t(" << 21. / i << ")\n";
}
```
Run your program to observe the output. 

$$\large{{\text{\color{red}In Desmos, respond to Prompt 1 on Screen 3}}}$$

In C++, when a decimal number has to be converted to an integer, the number is __truncated__: all the numbers after the decimal places are removed so only the integer part remains.

__\*\*Commit/Push to GitHub\*\*__ with commit message that matches the section heading: _2. Integer Truncation_.

### 3. More Math
In the following subsections, there are more examples of the math that can be performed in C++. 

Provided you have Commited/Pushed the previous section to GitHub, you can start fresh by deleting the code inside `main()`
(this will make it easier to read the output)

#### Modulus
Run this code:
```
cout << 10 % 3 << endl;
```
The `%` character is referred to as the __modulus__ operator. Before responding to the prompt, you may want to try more of your own examples.

$$\large{{\text{\color{red}In Desmos, respond to Prompt 1 on Screen 4}}}$$

#### Order of Operations
Run this code:
```
cout << 4 + 5 * 10 << endl;
cout << (4 + 5) * 10 << endl;
```

$$\large{{\text{\color{red}In Desmos, respond to Prompt 1 on Screen 5}}}$$

#### Increment and Decrement
Run this code and observe the ouput:
```
int num1 = 10;

++num1;
cout << num1 << endl;
--num1;
cout << num1 << endl;
```
Add the following code before `return 0;` and run it:
```
num1 = 10; // reset num1 back to 10
cout << endl; // blank line for readability
cout << num1++ << endl;
cout << num1 << endl;
```

$$\large{{\text{\color{red}In Desmos, respond to Prompt 1 on Screen 6}}}$$

Add this code and observe the output:
```
num1 = 10;
num1 += 50;
cout << num1 << endl;
num1 -= 50;
cout << num1 << endl;
```

$$\large{{\text{\color{red}In Desmos, respond to Prompt 2 on Screen 6}}}$$

__\*\*Commit/Push to GitHub\*\*__ with commit message that matches the section heading: _3. More Math_.

### 4. Wrap Up
You will always do these two steps:

1. Double-check you have properly committed/pushed all steps (view your change history on GitHub).
2. Read the _Notes.md_ and summarize the main points in your composition book.
