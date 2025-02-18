# **C++ Data Types**

A variable in **C++** must have a specified **data type**.

---

## **Basic Data Types**
The **data type** specifies the **size and type** of information the variable will store.

| **Data Type** | **Size**      | **Description** |
|--------------|--------------|----------------|
| `boolean`    | **1 byte**   | Stores `true` or `false` values |
| `char`       | **1 byte**   | Stores a single character/letter/number, or ASCII values |
| `int`        | **2 or 4 bytes** | Stores whole numbers, without decimals |
| `float`      | **4 bytes**   | Stores fractional numbers, containing one or more decimals. Sufficient for storing **6-7 decimal digits** |
| `double`     | **8 bytes**   | Stores fractional numbers, containing one or more decimals. Sufficient for storing **15 decimal digits** |

---

### **Example Usage in C++**
```cpp
#include <iostream>
using namespace std;

int main() {
    bool myBoolean = true;  // Boolean variable
    char myChar = 'A';      // Character variable
    int myInt = 100;        // Integer variable
    float myFloat = 9.99;   // Float variable
    double myDouble = 99.99999; // Double variable

    cout << "Boolean: " << myBoolean << endl;
    cout << "Character: " << myChar << endl;
    cout << "Integer: " << myInt << endl;
    cout << "Float: " << myFloat << endl;
    cout << "Double: " << myDouble << endl;

    return 0;
}

```

## C++ Numeric Data Types:

### Numeric Types
Use **int** when you need to store a whole number without decimals, like 35 or 1000, and **float** or **double** when you need a floating point number (with decimals), like 9.99 or 3.14515.

---

**Bro Code Data Types Code**

```cpp
#include <iostream>
using namespace std;

int main () {

    // Whole Numbers
    int age = 27;
    
    // double
    double height = 5.11;

    // char
    char gender = 'M';
    char earnings = '$';

    // Boolean
    bool fair = true;

    // Strings
    string firstname = "Mithun";
    string lastname = "Dama";

    cout << "Hello My First Name is " << firstname  << " and My age is " << age << " with height " << height <<"\n";
    cout << "Hello My Last Name Is: " << lastname << "\n";

    return 0;
}

```
