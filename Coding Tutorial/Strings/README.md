# C++ String Methods Explained Simply:

## 1. name.clear() – Clears the String:
This removes all characters from the string, making it empty **("")**.

```cpp
#include <iostream>
using namespace std;

int main() {

    string name;

    cout << "Enter your Name: ";
    getline(cin,name);  
    /* The getline() function in C++ is used to read an entire line of text,
     including spaces, until a newline (\n) or a specified delimiter is found.*/

    name.clear();
    cout << "Hello " << name;
    return 0;
}

```
----

