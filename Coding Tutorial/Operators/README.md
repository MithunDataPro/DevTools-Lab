# Operators:
Operators are symbols that tell the compiler what action to perform on variables or values.

## 1. Logical Operators (&&, ||, !):
These are used for decision-making (like in if conditions). They return true (1) or false (0).

#### ✅ AND Operator (&&) – Both conditions must be true:
```cpp
#include <iostream>
using namespace std;

int main() {

    int temp;
    cout << "Enter the Temperature: ";
    cin >> temp;

    if(temp >=0 && temp <=35) {
        cout << "The weather is Good";
    }
    else if(temp >= -100 && temp <= 0) {
        cout << "The weather is drastic! Kindly dont go Outside";
    }
    else {
        cout <<"The weather is Not Good";
    }
    return 0;
}

```
- ✅ true if both conditions are true.
- ❌ false if at least one condition is false.

#### ✅ OR Operator (||) – At least one condition must be true:
```cpp
#include <iostream>
using namespace std;

int main() {

    int temp;
    cout << "Enter the Temperature: ";
    cin >> temp;

    if(temp ==0 || temp >=0) {
        cout << "The weather is Good";
    }
    else {
        cout <<"The weather is Not Good";
    }
    return 0;
}

```
- ✅ true if at least one condition is true.
- ❌ false if both conditions are false.

#### ✅ NOT Operator (!) – Reverses a condition
```cpp
#include <iostream>
using namespace std;

int main() {

    int temp;
    bool sunny = true;
    cout << "Enter the Temperature: ";
    cin >> temp;

    if(temp <= 0 || temp >= 30) {
        cout << "The weather is bad" <<"\n";
    }
    else {
        cout <<"The weather is Good"<<"\n";
    }

    if(!sunny){
        cout << "It is sunny Outside!";
    }
    else{
        cout << "It is cloudy Outside";
    }
    return 0;
}

```
- ✅ true becomes false
- ❌ false becomes true

---












---

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
