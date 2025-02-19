## Understanding switch in C++ in Simple Words
In **C++**, the switch statement is like a decision-making tool that helps us choose between multiple options. It works like a menu, where each option leads to a different action.

**Example Calculator Program**

```cpp
// Calculator:

#include <iostream>
using namespace std;

int main() {
    char op;
    double num1;
    double num2;
    double result;

    cout << "***************** Calculator ***************** "<<"\n"; 

    cout << "Enter either (+, -, *, /): ";
    cin >> op;

    cout << "Enter the value of #1: ";
    cin >> num1;

    cout <<"Enter the value of #2: ";
    cin >> num2;

    switch(op){
        case '+':
              result = num1 + num2;
              cout << "Hence the Result is: " << result <<"\n";
              break;
        case '-':
              result = num1 - num2;
              cout << "Hence the Result is: " << result <<"\n";
              break;
        case '*':
              result = num1 * num2;
              cout << "Hence the Result is: " << result <<"\n";
              break;
        case '/':
              result = num1 / num2;
              cout << "Hence the Result is: " << result <<"\n";
              break;
        default:
              cout << "Enter the Valid Operator";
              break;

    }
cout << "**********************************************";
    return 0;

}

```
