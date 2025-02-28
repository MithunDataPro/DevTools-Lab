# Relationship between Virtual Functions, Pure Virtual Functions and Abstract Classes in OOP explained:

**Virtual functions, pure virtual functions, and abstract classes** are closely related concepts in **Object-Oriented Programming (OOP)** that enable polymorphism in C++. Let’s explore their definitions, differences, and relationships with examples.

## 1️⃣ Virtual Functions
**Definition:**
A virtual function is a member function in a base class that can be overridden in a derived class. It allows runtime polymorphism (i.e., function binding happens at runtime, not compile-time).

**Key Features:**
- ✅ Declared using the virtual keyword in the base class.
- ✅ Can have a default implementation.
- ✅ Allows overriding in derived classes.
- ✅ Enables dynamic binding using pointers or references to the base class.

#### My Version:
```cpp
// Virtual Function:
/*Virtual FUnction will execute the most derieved version of function when you invoke
   that function using base class pointer or refrence, the most derieved version of that
      function would be executed.*/
#include <iostream>
class School{
    public:
    // Virtual Function
    virtual void Syllabus(){
        std::cout << "School has 6 Subjects with 0 Labs..." << std::endl;
    };
        // std::cout << "School has 6 Subjects with 0 Labs...." << std::endl;
};
class College : public School{
    public:
    void Syllabus(){
        std::cout << "College has 7 Subjects with 6 Labs..." << std::endl;
    }
};
int main(){
// So Now it will execute the most derieved version.
// Base Class Pointed 
    School* child = new College();
    child ->Syllabus();
    return 0;
}

```

---

## 2️⃣ Pure Virtual Functions
**Definition:**
- A pure virtual function is a virtual function with no implementation in the base class.
- It forces derived classes to override the function.

```cpp
virtual void functionName() = 0;

```

(The = 0 makes it a pure virtual function.)

**Key Features:**
- ✅ Declared but NOT defined in the base class.
- ✅ Must be overridden in derived classes.
- ✅ Makes the class abstract (i.e., it cannot be instantiated).

---

## 3️⃣ Abstract Classes
**Definition:**
An abstract class is a class that has at least one pure virtual function. It cannot be instantiated and is meant to be inherited by derived classes.

**Key Features:**
- ✅ Contains at least one pure virtual function.
- ✅ Cannot be instantiated directly.
- ✅ Used as a base class for derived classes.
- ✅ Can have regular (non-virtual) functions as well.

##### My Version:
```cpp

// Pure Virtual Function:
#include <iostream>
// This Class has become an Abstract Class.
// Abstract Class: It Should Have atleast one pure virtual Function.
class School{
    public:
    // Pure Virtual Function
    virtual void Syllabus() = 0;
        // std::cout << "School has 6 Subjects with 0 Labs...." << std::endl;
};
class College : public School{
    public:
    void Syllabus(){
        std::cout << "College has 7 Subjects with 6 Labs..." << std::endl;
    }
};
class Intermediate: public School{
    public:
    void Syllabus(){
        std::cout << "Intermediate has Just 5 Subjects with 2 Labs..." << std::endl;
    }

};
int main(){
// So Now it will execute the most derieved version.
// Base Class Pointed 
    School* child = new College();
    child ->Syllabus();

    School* adult = new Intermediate();
    adult->Syllabus();
    return 0;
}

```
