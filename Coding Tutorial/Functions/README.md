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
## Function by Reading data from other function:

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
# Return Functions:

```cpp
// return keyword:
// return = return a value back to the spot where you called
//          the encompassing function.

#include <iostream>
using namespace std;

// Now lets find circumferance of a circle 

double circle(double radius, double pie); // Now we chnaged void to double because of the o/p we need

int main(){   // this is our main function

    double radius;
    double pie;
    cout << "Enter the Radius: ";
    cin >> radius;

    cout << "Enter the value of Pie: ";
    cin >> pie;

    double result = circle(radius, pie);

    cout << "Circumference of a circle is: " << circle << " Units";

    return 0;

}

double circle(double radius, double pie){
    return 2 * pie * radius;
}

```

---
