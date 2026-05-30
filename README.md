# ✅ Input & Validation Library

A lightweight C++ input validation utility class that provides static methods for validating and safely reading numeric and date inputs from the user.

---

## 📖 Overview

`clsInputValidate` is a reusable C++ class that simplifies input handling by combining type-safe reading with range validation. It depends on `clsString` and `clsDate` and is designed to be used across projects that require robust user input handling.

---

## ✨ Features

- **Range Validation**: Check if a number or date falls within a specified range
- **Safe Integer Reading**: Read an integer from the user with automatic error handling on invalid input
- **Safe Double Reading**: Read a double from the user with automatic error handling on invalid input
- **Bounded Input Reading**: Read an integer or double guaranteed to be within a given range
- **Date Validation**: Validate a date using `clsDate` rules including leap year support
- **Date Range Check**: Check if a date falls between two other dates in either direction

---

## 🚀 How to Use

Include the header file in your project:

```cpp
#include "clsInputValidate.h"
```

### Number Validation
```cpp
bool valid = clsInputValidate::IsNumberBetween(5, 1, 10);  // true
```

### Safe Input Reading
```cpp
int age = clsInputValidate::ReadIntNumber("Invalid! Enter again: ");

int choice = clsInputValidate::ReadIntNumberBetween(1, 5, "Choose between 1 and 5: ");

double salary = clsInputValidate::ReadDblNumberBetween(1000.0, 9999.9);
```

### Date Validation & Range
```cpp
clsDate D(29, 2, 2024);
bool isValid = clsInputValidate::IsValideDate(D);  // true (leap year)

bool inRange = clsInputValidate::IsDateBetween(
    clsDate(15, 6, 2024),
    clsDate(1, 1, 2024),
    clsDate(31, 12, 2024)
);  // true
```

---

## 🧠 Concepts Used

- **OOP** — All methods encapsulated as static members inside a class
- **Static Methods** — Callable without creating an instance
- **Method Overloading** — `IsNumberBetween()` supports short, int, float, and double
- **Input Stream Handling** — Uses `cin.clear()` and `cin.ignore()` to recover from invalid input
- **Default Parameters** — Custom or default error messages for all read functions
- **Dependency** — Uses `clsDate` for date validation and comparison logic
- **Loops** — Used to keep prompting the user until valid input is received

---

## 🔑 Key Methods

| Method | Description |
|---|---|
| `IsNumberBetween()` | Checks if a number (short/int/float/double) is within a range |
| `IsDateBetween()` | Checks if a date falls between two other dates in either direction |
| `ReadIntNumber()` | Safely reads an integer with error handling on invalid input |
| `ReadIntNumberBetween()` | Reads an integer guaranteed to be within a specified range |
| `ReadDblNumber()` | Safely reads a double with error handling on invalid input |
| `ReadDblNumberBetween()` | Reads a double guaranteed to be within a specified range |
| `IsValideDate()` | Validates a date using `clsDate` rules |

---

## 📄 License

This project is open source and free to use for educational purposes.

---

## 👤 Author

👤 **Mahmoud Abd El-Sattar**  
📧 mahmoud.abdelsattar.dev@gmail.com  
💼 [linkedin.com/in/mahmoud-abd-el-sattar](https://www.linkedin.com/in/mahmoud-abd-el-sattar-1b227522a)
