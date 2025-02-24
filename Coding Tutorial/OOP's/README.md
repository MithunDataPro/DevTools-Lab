# Object Oriented Programming in C++

Object-oriented programming – As the name suggests, uses objects in programming. Object-oriented programming aims to implement real-world entities like **inheritance, hiding, polymorphism**, etc., in programming. The main aim of OOP is to bind together the **data and the functions** that operate on them so that no other part of the code can access this data except that function.

There are some basic concepts that act as the **building blocks of OOP**, i.e.:

- **Class**
- **Object**
- **Encapsulation**
- **Abstraction**
- **Polymorphism**
- **Inheritance**
- **Dynamic Binding**
- **Message Passing**

## Characteristics of an Object-Oriented Programming Language

![image](https://github.com/user-attachments/assets/5a7be83c-e5e9-4bab-be50-3bd2d312b94e)


### **Class**
The building block of C++ that leads to Object-Oriented programming is a **Class**. It is a **user-defined data type**, which holds its own **data members and member functions**, which can be accessed and used by creating an **instance** of that class. A class is like a **blueprint** for an object. 

#### **Example**:
Consider the **Class of Cars**. There may be many cars with different names and brands, but all of them will share some common properties like:
- All of them will have **4 wheels**.
- **Speed Limit**.
- **Mileage range**.

So here, the **Car** is the **class**, and **wheels, speed limits, and mileage** are their **properties**.

- A **Class** is a **user-defined data type** that has **data members and member functions**.
- **Data members** are the **data variables**, and **member functions** are the **functions** used to manipulate these variables.
- Together, these **data members** and **member functions** define the **properties and behavior** of the **objects** in a Class.

In the **above example** of class **Car**:
- The **data members** will be **speed limit, mileage**, etc.
- The **member functions** can be **apply brakes, increase speed**, etc.

We can say that a **Class in C++** is a **blueprint** representing a **group of objects** that share some **common properties and behaviors**.

---

### **Object**
An **Object** is an **identifiable entity** with some **characteristics and behavior**. An **Object** is an **instance** of a **Class**. When a **class** is defined, **no memory is allocated**, but when it is **instantiated** (i.e., an **object is created**), **memory is allocated**.

```cpp
// C++ Program to show the syntax/working of Objects as a
// part of Object Oriented PProgramming
#include <iostream>
using namespace std;

class person {
    char name[20];
    int id;

public:
    void getdetails() {}
};

int main()
{

    person p1; // p1 is a object
    return 0;
}

```

Objects take up space in memory and have an associated address like a record in pascal or structure or union. When a program is executed the objects interact by sending messages to one another. Each object contains data and code to manipulate the data. Objects can interact without having to know details of each other’s data or code, it is sufficient to know the type of message accepted and the type of response returned by the objects.

---

### Encapsulation:
In normal terms, Encapsulation is defined as wrapping up data and information under a single unit. In Object-Oriented Programming, Encapsulation is defined as binding together the data and the functions that manipulate them. Consider a real-life example of encapsulation, in a company, there are different sections like the accounts section, finance section, sales section, etc. The finance section handles all the financial transactions and keeps records of all the data related to finance. Similarly, the sales section handles all the sales-related activities and keeps records of all the sales. Now there may arise a situation when for some reason an official from the finance section needs all the data about sales in a particular month. In this case, he is not allowed to directly access the data of the sales section. He will first have to contact some other officer in the sales section and then request him to give the particular data. This is what encapsulation is. Here the data of the sales section and the employees that can manipulate them are wrapped under a single name **“sales section”**.

![image](https://github.com/user-attachments/assets/279136af-7dac-4843-a187-63800539ac69)

Encapsulation also leads to data abstraction or data hiding. Using encapsulation also hides the data. In the above example, the data of any of the sections like sales, finance, or accounts are hidden from any other section.

---

### Abstraction:
Data abstraction is one of the most essential and important features of object-oriented programming in C++. Abstraction means displaying only essential information and hiding the details. Data abstraction refers to providing only essential information about the data to the outside world, hiding the background details or implementation. Consider a real-life example of a man driving a car. The man only knows that pressing the accelerator will increase the speed of the car or applying brakes will stop the car but he does not know how on pressing the accelerator the speed is actually increasing, he does not know about the inner mechanism of the car or the implementation of an accelerator, brakes, etc. in the car. This is what abstraction is.

- **Abstraction using Classes:** We can implement Abstraction in C++ using classes. The class helps us to group data members and member functions using available access specifiers. A Class can decide which data member will be visible to the outside world and which is not.
- **Abstraction in Header files:** One more type of abstraction in C++ can be header files. For example, consider the pow() method present in math.h header file. Whenever we need to calculate the power of a number, we simply call the function pow() present in the math.h header file and pass the numbers as arguments without knowing the underlying algorithm according to which the function is actually calculating the power of numbers.

---

### Polymorphism
The word polymorphism means having many forms. In simple words, we can define polymorphism as the ability of a message to be displayed in more than one form. A person at the same time can have different characteristics. A man at the same time is a father, a husband, and an employee. So the same person possesses different behavior in different situations. This is called polymorphism. An operation may exhibit different behaviors in different instances. The behavior depends upon the types of data used in the operation. C++ supports operator overloading and function overloading.

- **Operator Overloading:** The process of making an operator exhibit different behaviors in different instances is known as operator overloading.
- **Function Overloading:** Function overloading is using a single function name to perform different types of tasks. Polymorphism is extensively used in implementing inheritance.



**Example:** Suppose we have to write a function to add some integers, sometimes there are 2 integers, and sometimes there are 3 integers. We can write the Addition Method with the same name having different parameters, the concerned method will be called according to parameters. 

![image](https://github.com/user-attachments/assets/e8f63b68-2592-457b-8a4d-15a51136b033)

---

### Inheritance
The capability of a class to derive properties and characteristics from another class is called Inheritance. Inheritance is one of the most important features of Object-Oriented Programming.

- **Sub Class:** The class that inherits properties from another class is called Sub class or Derived Class.
- **Super Class:** The class whose properties are inherited by a sub-class is called Base Class or Superclass.
- **Reusability:** Inheritance supports the concept of “reusability”, i.e. when we want to create a new class and there is already a class that includes some of the code that we want, we can derive our new class from the existing class. By doing this, we are reusing the fields and methods of the existing class.


**Example:** Dog, Cat, Cow can be Derived Class of Animal Base Class.

![image](https://github.com/user-attachments/assets/fca71d35-1bd6-46ed-ad76-591dd5c4b95a)

---

### Dynamic Binding
In dynamic binding, the code to be executed in response to the function call is decided at runtime. C++ has virtual functions to support this. Because dynamic binding is flexible, it avoids the drawbacks of static binding, which connected the function call and definition at build time.

**Example:**

```cpp
// C++ Program to Demonstrate the Concept of Dynamic Binding without virtual function
#include <iostream>
using namespace std;

class GFG {
public:
    void call_Function() // function that calls print
    {
        print();
    }
    void print() // the display function
    {
        cout << "Printing the Base class Content" << endl;
    }
};

class GFG2 : public GFG // GFG2 inherits publicly from GFG
{
public:
    void print() // GFG2's display
    {
        cout << "Printing the Derived class Content" << endl;
    }
};

int main()
{
    GFG* geeksforgeeks = new GFG(); // Creating GFG's object using pointer
    geeksforgeeks->call_Function(); // Calling call_Function

    GFG* geeksforgeeks2 = new GFG2(); // creating GFG2 object using pointer
    geeksforgeeks2->call_Function(); // calling call_Function for GFG2 object

    delete geeksforgeeks;
    delete geeksforgeeks2;

    return 0;
}

```

**Output:**
```
Printing the Base class Content
Printing the Base class Content

```
As we can see, the print() function of the parent class is called even from the derived class object. To resolve this we use virtual functions.

**Above Example with virtual Function:**

```cpp
// C++ Program to Demonstrate the Concept of Dynamic binding
// with the help of virtual function

#include <iostream>
using namespace std;

class GFG
{
  public:
    // using "virtual" for the display function
    virtual void print()
    {
        cout << "Printing the Base class Content" << endl;
    }
    // function that calls print
    void call_Function()
    {
        print();
    }
};
// GFG2 inherits publicly from GFG
class GFG2 : public GFG
{
  public:
    // GFG2's display
    void print() override
    {
        cout << "Printing the Derived class Content" << endl;
    }
};

int main()
{
    // Creating GFG's object using pointer
    GFG *geeksforgeeks = new GFG();
    // Calling call_Function
    geeksforgeeks->call_Function();

    // creating GFG2 object using pointer
    GFG *geeksforgeeks2 = new GFG2();
    // calling call_Function for GFG2 object
    geeksforgeeks2->call_Function();

    delete geeksforgeeks;
    delete geeksforgeeks2;

    return 0;
}

```

**Output:**
```
Printing the Base class Content
Printing the Derived class Content

```

---

### Message Passing:
Objects communicate with one another by sending and receiving information. A message for an object is a request for the execution of a procedure and therefore will invoke a function in the receiving object that generates the desired results. Message passing involves specifying the name of the object, the name of the function, and the information to be sent.

**Example:**

```cpp
#include <iostream>
using namespace std;

// Define a Car class with a method to display its speed
class Car {
public:
    void displaySpeed(int speed) {
        cout << "The car is moving at " << speed << " km/h." << endl;
    }
};

int main() {
    // Create a Car object named myCar
    Car myCar;

    // Send a message to myCar to execute the displaySpeed method
    int currentSpeed = 100;
    myCar.displaySpeed(currentSpeed);

    return 0;
}

//this code is contributed by Md Nizamuddin

```
---

#### Advantage of OOPs over Procedure-oriented programming language
Here are key advantages of Object-Oriented Programming (OOP) over Procedure-Oriented Programming (POP):

- **1. Modularity and Reusability:** OOP promotes modularity through classes and objects, allowing for code reusability.
- **2. Data Encapsulation:** OOP encapsulates data within objects, enhancing data security and integrity.
- **3. Inheritance:** OOP supports inheritance, reducing redundancy by reusing existing code.
- **4. Polymorphism:** OOP allows polymorphism, enabling flexible and dynamic code through method overriding.
- **5. Abstraction:** OOP enables abstraction, hiding complex details and exposing only essential features
