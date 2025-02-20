# Function:
A Function is Block of Reusable Code.

```cpp
// functions = A Block Of Reusable Code

#include <iostream>
using namespace std;

void mithundama () {
    cout << "He is Great Man" << "\n";
    cout << "He is Greatest of all time" << "\n";
    cout << "He is a real legend" << "\n";
    cout << "He is Great Man" << "\n";
    cout << "He is Great Man" << "\n\n";

}

int main() {
    mithundama();
    mithundama();
    mithundama();
    mithundama();
    return 0;
}

```
## FUnction by Reading data from other function:

```cpp
#include <iostream>
using namespace std;

void election(string state);


int main() {
    string state = "Andhra Pradesh";

    election(state);

    return 0;

}

void election(string state){  // We need to define data type with its name to read data from other function.
    int age;
    char sex;

    cout << "What is your age: ";
    cin >> age;
    
    cout << "What is Your Sex: ";
    cin >> sex;

    if(age >= 18 && age <= 99 && (sex == 'M' || sex == 'm')) {
        cout << "You are Male and you are elgible to vote in " <<state  <<"\n";
    }
    else if(age >=18 && age <=99 && (sex == 'F' || sex == 'f')){
        cout << "You are a Female and You are Elgible to vote in " <<state <<"\n";
    }
    else if(age >=100){
        cout << "Your age is too high to vote in " <<state <<"\n";
    }
    else{
        cout <<"you are not elgible to vote in " <<state <<"\n";
    }
}

```
