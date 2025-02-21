## Passing an Array to a Function in C++
In C++, you cannot pass an entire array as a function parameter. Instead, you pass its reference (pointer) or use std::vector. There are three common ways:

### 1️⃣ Pass an Array Using a Pointer
### 2️⃣ Pass an Array Using Reference (&)
### 3️⃣ Pass an Array Using std::vector (Recommended)

```cpp
// Passing Array to Function
#include <iostream>
#include <vector>
#include <cmath>
using namespace std;

double getTotal(double scores[], int size);

int main() {

    // Lets Calculate the Cricket Scores to Contribute to team Total
    double scores [] = {87,23,100,34,76,98,100};
    string player[] = {"Rohith","Shubham","Virat","Hardik","Rahul","Shreyas","Jadeja"};
    int size = sizeof(scores)/sizeof(double);
    double total = getTotal(scores, size);
    cout << "***********************************************************\n";
    cout << "****************** Welcome To Cricket *********************\n";
    cout << "***********************************************************\n";

    cout << "Total Team Score: "<< total << "\n";
    
    return 0;
}
double getTotal(double scores[],int size){
    double total = 0;
    for (int i =0; i < size; i++){
        total += scores[i];
    }
    return total;
}

```

---

## Search an array for an Element:

```cpp
#include <iostream>

int searchArray(int array[], int size, int element);

int main(){

    int numbers[] ={1,2,3,4,5,6,7,8,9,10};
    int size = sizeof(numbers)/sizeof(int);
    int index;
    int myNum;

    std:: cout << "Enter element to search for: " << "\n";
    std:: cin >> myNum;

    index = searchArray(numbers, size, myNum);

    if(index != -1){
        std:: cout << myNum << " Is at index " << index;
    }
    else{
        std::cout << myNum << " Is not in array.";
    }


    return 0;
}

int searchArray(int array[], int size, int element){
    for(int i=0; i < size; i++){
        if(array[i] == element){
            return i;
        }
    }
    return -1;
  }  // in programming -1 refers as centimental value. that means something is not found.

```

### For Strings:

```cpp
#include <iostream>
using namespace std;

int searchArray(string array[], int size, string element);

int main(){

    std:: string heros[] ={"PSPK","Mahesh Babu","NTR","Prabhas_Raju","Ram Charan","Allu Arjun"};
    int size = sizeof(heros)/sizeof(std::string);
    int index;
    std::string myhero;

    std:: cout << "Enter Hero Name to search for who is Top Actor in TFI: ";
    std::getline(cin , myhero);

    index = searchArray(heros, size, myhero);

    if(index != -1){
        std:: cout << myhero << " Is at index " << index;
    }
    else{
        std::cout << myhero << " Is not in array.";
    }


    return 0;
}

int searchArray(string array[], int size, string element){
    for(int i=0; i < size; i++){
        if(array[i] == element){
            return i;
        }
    }
    return -1;
  }  // in programming -1 refers as centimental value. that means something is not found.

```
