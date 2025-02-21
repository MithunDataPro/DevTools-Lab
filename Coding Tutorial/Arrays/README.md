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
