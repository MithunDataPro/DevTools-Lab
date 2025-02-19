# While Loop:
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
