## Ternary Operator (?:) in C++ – Explained Simply
The **ternary operator** in C++ is a shortcut for an if-else statement. It allows you to write a simple decision in just one line.

### Basic Syntax
```cpp
condition ? expression_if_true : expression_if_false;

```
- If **condition** is true, it executes **expression_if_true**.
- If **condition** is false, it executes **expression_if_false**.

---

## Example 1: A Person Can Vote or not

```cpp
#include <iostream>
using namespace std;

int main() {

    int age;
    cout << "what is your age: ";
    cin >> age;
    

    age>=18 ? cout <<"You are elgible to vote" : cout<<"You are not elgible to vote";
    return 0;
}

```
