# Banking Program For Beginners:

```cpp
#include <iostream>
#include <iomanip>   // function to manipulate output
using namespace std;

void showBalance(double balance);
double deposit();
double withdraw(double balance);

int main() {
    double balance = 0;
    int choice = 0;
    string Name;

    do{
    cout << "************************************" <<"\n";
    cout << "********* Welcome to Bank Of America *********"<<"\n";
    cout <<"****************************************"<<"\n";
    cout <<"Enter Your Name: ";
    getline(cin, Name);
    cout <<"How can we Help you Today: " << Name <<"\n"; 
    cout <<"Enter your Choice" << "\n";
    cout << "1. Show Balance\n";
    cout << "2. Deposit Money\n";
    cout << "3. Withdraw Money\n";
    cout << "4. Exit\n";
    cin >> choice;

    cin.clear(); 
    fflush(stdin);

    switch(choice){
        case 1: showBalance(balance);
        break;
        case 2: balance += deposit();
                showBalance(balance);
        break;
        case 3: balance -= withdraw(balance);
                showBalance(balance);
        break;
        case 4: cout << "Thanks For Visiting";
        break;
        deafult: cout << "Please enter a Valid case Number\n";
    }

    }while(choice != 4);
    return 0;
}

void showBalance(double balance){
    cout << "Your Balance is: $" << setprecision(3) << fixed << balance <<"\n";
    // There us a Function to set Precision after the output 

}
double deposit(){
    double amount =0;
    cout << "Enter the amount to be deposited: ";
    cin >> amount;
    if(amount>=0){
        return amount;
    }
    else{
        cout << "That's not a Valid Amount" <<"\n";
    }
}

double withdraw(double balance){
    double amount = 0;
    cout << "Enter amount to be withdrawn: ";
    cin >> amount;
    if(amount > balance){
        cout << "You Have Insuffcient Funds " << "\n";
        return 0;
    }
    else if(amount < 0){
        cout << "Thats not a Valid Amount\n";
        return 0;
    }
    else{
        return amount;
    }
}

```
