## 1. What is an Exception?
An **exception** is an error that occurs during the execution of a program. Instead of crashing the program, C++ provides a way to handle such errors using **exception handling mechanisms.**

#### Key Points for Exam:
- ✅ Exceptions are runtime errors (they occur during execution, not compilation).
- ✅ They allow us to separate error-handling code from normal code.
- ✅ If an exception is not handled properly, the program will terminate.
- ✅ C++ provides the try-catch mechanism to handle exceptions.

## 2. Catching and Throwing Exceptions
**C++ provides three keywords for exception handling:**
- 🔹 try – Defines a block where an exception might occur.
- 🔹 throw – Used to signal an exception.
- 🔹 catch – Handles the exception.

**Basic Syntax**
```cpp
try {
    // Code that may cause an exception
} 
catch (exceptionType identifier) {
    // Code to handle the exception
}

```

#### Exam Takeaways:
- ✅ throw is used to raise an exception.
- ✅ catch handles exceptions and prevents crashes.
- ✅ The program continues execution after exception handling.

## 3. Different Classes and Hierarchy of Exceptions
C++ has a built-in exception hierarchy under the **std::exception** class.

**Hierarchy of Standard Exceptions:**
```cpp

std::exception
│
├── std::logic_error
│   ├── std::invalid_argument
│   ├── std::domain_error
│   ├── std::length_error
│   ├── std::out_of_range
│
├── std::runtime_error
│   ├── std::overflow_error
│   ├── std::underflow_error
│   ├── std::range_error
│   ├── std::system_error

```

#### Example:
```cpp
#include <iostream>
#include <stdexcept>     // Required For Standard Exception's.
#include <string>
#include <list>  
using namespace std;

class Printer{                         // By Default Class is Private
    string Name;
    int Available_paper;  
public:
Printer(string name, int paper){  // This Printer Constructor will Recieve Two Parameters
    Name = name;
    Available_paper = paper;                              
        }
    void print(string txtdoc){
        int required_paper = txtdoc.length()/10;  // If we Take Sample txtdoc 40/10=4
        if(required_paper > Available_paper)
        throw "No Paper";
        
        cout <<"Printing... " << txtdoc << endl;
        Available_paper -= required_paper;

    }
};
int main(){
    Printer myprint("Epson",10);
    try{
        myprint.print("Hello My Name is Mithun.. I am a Software Engineer");
    myprint.print("Hello My Name is Mithun.. I am a Software Engineer");
    myprint.print("Hello My Name is Mithun.. I am a Software Engineer");
    }
    catch (const char * txtException){
        cout << "Exception: " << txtException << endl;
    }
    // To handle Int DataTypes in Throw
    catch (int exCode){
        cout << "Exception: " << exCode << endl ;
    }
    // Default Handler
    catch(...){
        cout << "Exception Handeled!" << endl;
    }
    
    system("pause>nul");
    return 0;
}

```
