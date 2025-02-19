# While Loop:

While Some Condition is True then you will continue to execute something.

```cpp
#include <iostream>
using namespace std;

int main() {
    string name;

    // Now Using While Loop
    while(name.empty()){
        cout << "Enter your name: ";
        getline(cin,name);
    }

    cout << "Hello " << name;
    return 0;
}

```
---

# Do While Loop
Do some Block of code sirst then repeat again if condition is true.

```cpp
#include <iostream>
using namespace std;

int main() {

    int number;

    do{
        cout <<"Enter a Positive Number: ";
        cin >> number;
    }while(number<0);

    cout <<"The +ve Number is: " << number;
    return 0;
}

```

---

# For Loop:
A for loop in C++ is used to repeat a block of code a specific number of times. It is mostly used when you know how many times you need to repeat the task.

#### ✅ Basic Syntax of for Loop:
```cpp
for(initialization; condition; update) {
    // Code to execute
}

```
- **Initialization:** Runs once at the start (e.g., int i = 0).
- **Condition:** Checked before each loop iteration. If true, the loop continues.
- **Update:** Runs after each iteration (e.g., i++ to increase i).

```cpp
#include <iostream>
using namespace std;

int main() {
    for(int i = 2; i <= 100; i+=2){
        cout<< i ;
    }
    cout << "Ended";
    return 0;
}

```
---

## Nested Loop:
Nested Loops in C++ – Explained Simply
A nested loop is a loop inside another loop. The inner loop executes completely every time the outer loop runs once.

```cpp
// Nested Loops
// So Now we are printing a rectangle that made of symbols.

#include <iostream>
using namespace std;

int main() {
    int rows;
    int columns;
    char symbol;

    cout << "How many rows?: ";
    cin >> rows;

    cout << "How many columns?: ";
    cin >> columns;

    cout <<"Enter a symbol to use: ";
    cin >> symbol;

    for(int i = 1; i <= rows; i++){
        for(int j = 1; j <= columns; j++){
            cout << symbol;
        }
        cout << "\n";
    }
    return 0;
}

```
