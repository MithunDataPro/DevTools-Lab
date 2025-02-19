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
