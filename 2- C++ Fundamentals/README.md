# **C++ Basic Concepts Documentation (Expanded Version)**

This document covers essential C++ concepts including program structure, variables, data types, operators, input/output, and characters. Each topic includes detailed explanations, rules, examples, and outputs.

---

## **1. Basic Structure of a C++ Program and Special Header Files**

A C++ program has a standard structure that must be followed for successful compilation and execution.

### **1.1 Structure Example**

```cpp
#include <iostream>   // Standard library header for input-output operations

using namespace std;  // Use the standard namespace

int main() {
    cout << "Hello, World!" << endl;  // Output statement
    return 0;                          // Exit code indicating successful execution
}
```

### **1.2 Components Explained**

1. **Header Files**

   * Introduced using `#include`.
   * Provide access to predefined classes, functions, and macros.
   * Example: `#include <iostream>` allows using `cin`, `cout`, and `endl`.

2. **Namespace**

   * C++ groups functions and objects into namespaces to avoid naming conflicts.
   * `using namespace std;` allows direct access to standard library names without prefixing `std::`.

3. **`main()` Function**

   * Entry point of the program.
   * Return type is `int` (returns integer value to OS).
   * Example: `return 0;` indicates the program executed successfully.

4. **Statements**

   * Each statement ends with a semicolon (`;`).
   * Statements inside `{}` form the **body** of the function.

---

## **2. Understanding `cout`**

`cout` is the standard output stream used to display information on the console.

### **2.1 Syntax**

```cpp
cout << "message";
```

* `<<` is the **insertion operator**, sending data to the output stream.
* Multiple items can be printed in sequence:

```cpp
cout << "Hello " << "World" << endl;
```

### **2.2 Example with Variables**

```cpp
#include <iostream>
using namespace std;

int main() {
    int age = 20;
    cout << "Your age is: " << age << endl;
    return 0;
}
```

**Output:**

```
Your age is: 20
```

* `endl` adds a newline and flushes the output buffer.

### **2.3 Tips**

* Use `cout` for all user-facing outputs.
* Multiple `<<` operators can chain messages and variables.

---

## **3. Variables**

Variables are named storage locations in memory.

### **3.1 Declaration and Initialization**

```cpp
int age = 25;      // integer variable
float height = 5.9; // floating-point variable
char grade = 'A';   // character variable
bool isPassed = true; // boolean variable
```

### **3.2 Rules for Naming Variables**

1. Must start with a letter or underscore (`_`), not a number.
2. Can include letters, digits, and underscores.
3. Case-sensitive (`age` ≠ `Age`).
4. Cannot use reserved keywords (like `int`, `return`).

---

## **4. Data Types**

C++ provides several data types to store different kinds of values.

### **4.1 Primary Data Types**

| Type     | Size    | Description                        |
| -------- | ------- | ---------------------------------- |
| `int`    | 4 bytes | Integer numbers                    |
| `float`  | 4 bytes | Decimal numbers (single precision) |
| `double` | 8 bytes | Decimal numbers (double precision) |
| `char`   | 1 byte  | Single character                   |
| `bool`   | 1 byte  | `true` or `false`                  |

### **4.2 Example**

```cpp
int a = 10;
float b = 3.14;
double c = 2.718281828;
char d = 'X';
bool e = false;

cout << "Int: " << a << ", Float: " << b << endl;
```

**Output:**

```
Int: 10, Float: 3.14
```

---

## **5. Simple Operators**

Operators perform operations on variables or values.

### **5.1 Arithmetic Operators**

| Operator | Meaning        | Example                      |
| -------- | -------------- | ---------------------------- |
| `+`      | Addition       | 5 + 3 = 8                    |
| `-`      | Subtraction    | 5 - 3 = 2                    |
| `*`      | Multiplication | 5 \* 3 = 15                  |
| `/`      | Division       | 5 / 2 = 2 (integer division) |
| `%`      | Modulo         | 5 % 2 = 1                    |

### **5.2 Example**

```cpp
int a = 10, b = 3;
cout << "Addition: " << a + b << endl;
cout << "Subtraction: " << a - b << endl;
cout << "Multiplication: " << a * b << endl;
cout << "Division: " << a / b << endl;
cout << "Modulo: " << a % b << endl;
```

**Output:**

```
Addition: 13
Subtraction: 7
Multiplication: 30
Division: 3
Modulo: 1
```

---

## **6. Modulo Operator `%`**

Returns the remainder of division. Only works with integers.

```cpp
int x = 17, y = 5;
cout << x % y << endl;  // Output: 2
```

**Rules:**

* Dividend sign affects the result in C++.
* Useful for checking even/odd numbers (`n % 2`).

---

## **7. Increment (`++`) and Decrement (`--`) Operators**

### **7.1 Pre vs Post**

| Type           | Meaning                         | Example | Output |
| -------------- | ------------------------------- | ------- | ------ |
| Pre-increment  | Increment first, then use value | `++x`   | 6      |
| Post-increment | Use value first, then increment | `x++`   | 5      |
| Pre-decrement  | Decrement first, then use value | `--x`   | 4      |
| Post-decrement | Use value first, then decrement | `x--`   | 5      |

### **Example**

```cpp
int a = 5;
cout << a++ << endl;  // Output: 5
cout << a << endl;    // Output: 6
cout << ++a << endl;  // Output: 7
```

---

## **8. Relational Operators**

Compare values and return `true` (1) or `false` (0).

| Operator | Description      | Example |
| -------- | ---------------- | ------- |
| `==`     | Equal to         | a == b  |
| `!=`     | Not equal to     | a != b  |
| `>`      | Greater than     | a > b   |
| `<`      | Less than        | a < b   |
| `>=`     | Greater or equal | a >= b  |
| `<=`     | Less or equal    | a <= b  |

**Example**

```cpp
int a = 5, b = 10;
cout << (a == b) << endl; // Output: 0
cout << (a < b) << endl;  // Output: 1
```

---

## **9. Characters and ASCII**

Each character has a numeric **ASCII code**.

```cpp
char ch = 'A';
cout << ch << endl;       // Output: A
cout << int(ch) << endl;  // Output: 65
```

**Common ASCII Codes:**

* `'A'` → 65, `'Z'` → 90
* `'a'` → 97, `'z'` → 122
* `'0'` → 48, `'9'` → 57

**Tips:**

* You can perform arithmetic with characters: `'A' + 1` → `'B'`.

---

## **10. Understanding `cin`**

`cin` is used to take input from the user via the keyboard.

### **10.1 Syntax**

```cpp
cin >> variable;
```

* `>>` is the extraction operator.

### **10.2 Example**

```cpp
#include <iostream>
using namespace std;

int main() {
    int age;
    cout << "Enter your age: ";
    cin >> age;
    cout << "You entered: " << age << endl;
    return 0;
}
```

**Sample Run:**

```
Enter your age: 21
You entered: 21
```

### **10.3 Multiple Inputs**

```cpp
int a, b;
cin >> a >> b;  // User enters: 5 10
cout << a << " " << b;  // Output: 5 10
```

**Tips:**

* Input stops at whitespace (space, tab, newline).
* Always validate input for robust programs.

---


