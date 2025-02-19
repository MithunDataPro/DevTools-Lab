# Experiemnets:

### Example 1: Temperature Conversion Program:
```cpp
// Now lets Write a Temperature Conversion Code:

#include <iostream>
using namespace std;

int main() {
    double temp;
    char unit;

    cout << "*********** Temperature Conversion Program **************" << "\n";

       cout << "F = Fahrenheit" << "\n\n";
       cout << "C =  Celsius" << "\n\n";
       cout << "What Unit You would like to convert to: ";
       cin >> unit;

       if(unit == 'F' || unit == 'f'){
        cout << "Enter the Temperature In Celcius: ";
        cin >> temp;
        temp = (1.8 * temp) + 32.0;
        cout << "Converted Temperature is: " << temp << "\n";
        }
       else if (unit == 'C' || unit == 'c') {
        cout << "Enter the Temperature In Fahrenheit: ";
        cin >> temp;
        temp = (temp - 32) / 1.8;
        cout << "Converted Temperature is: " << temp << "\n";
       }
       else {
        cout << "Enter the Temperature Value only in C or F";
       }
     cout << "****************** End ***********************************";
     return 0;

}

```
