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

## 2. name.length() / name.size() – Get Length of String
Returns the number of characters in the string.

```cpp
#include <iostream>
using namespace std;

int main() {

    string name;

    cout << "Enter your Name: ";
    getline(cin,name);  
    /* The getline() function in C++ is used to read an entire line of text,
     including spaces, until a newline (\n) or a specified delimiter is found.*/
    cout << name.length();
    return 0;
}

```
---
## Another Example:
```cpp
#include <iostream>
using namespace std;

int main() {

    string name;

    cout << "Enter your Name: ";
    getline(cin,name);  
    /* The getline() function in C++ is used to read an entire line of text,
     including spaces, until a newline (\n) or a specified delimiter is found.*/
    if (name.length() > 12) {
        cout << "Your Name Can't be more than 12 characters";
    }
    else{
        cout <<"Welcome " << name;
    }
    return 0;
}

```
**or**

```cpp
#include <iostream>
using namespace std;

int main() {

    string name;

    cout << "Enter your Name: ";
    getline(cin,name);  
    /* The getline() function in C++ is used to read an entire line of text,
     including spaces, until a newline (\n) or a specified delimiter is found.*/
    cout << name.size();
    return 0;
}

```
---

