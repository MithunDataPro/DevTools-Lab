# New Lines

**To insert a new line in your output, you can use the \n character:**

```cpp
#include <iostream>
using namespace std;

int main() {
cout << "I Love Coding \n";
cout << "We can also use for line space" << "\n";
cout <<"To get a Blank Line we can use Two New Line Characters" << "\n\n";
cout <<"Another way to insert a new line, is with the endl manipulator" <<endl;
cout <<"Both \n and endl are used to break lines. However, \n is most used.";
return 0;
}

```

### But what is \n exactly?
**The newline character (\n)** is called an **escape sequence**, and it forces the cursor to change its position to the beginning of the next line on the screen. This results in a new line.

**Examples of other valid escape sequences are:**
- \t - Creates a horizontal tab
- \\	Inserts a backslash character (\)
- \"	Inserts a double quote character


---

## C++ Comments
Comments can be used to explain C++ code, and to make it more readable. It can also be used to prevent execution when testing alternative code. Comments can be singled-lined or multi-lined.

### Single-line Comments
- Single-line comments start with two forward slashes (//).
- Any text between // and the end of the line is ignored by the compiler (will not be executed).
- This example uses a single-line comment before a line of code:

```cpp
// This is a comment
cout << "Hello World!";

```

- This example uses a single-line comment at the end of a line of code:
```cpp
cout << "Hello World!"; // This is a comment

```

### C++ Multi-line Comments
- Multi-line comments start with /* and ends with */.
- Any text between /* and */ will be ignored by the compiler:

```cpp
/* The code below will print the words Hello World!
to the screen, and it is amazing */
cout << "Hello World!";

```

**Note:**
**Single or multi-line comments?**
- It is up to you which you want to use. Normally, we use // for short comments, and /* */ for longer.

---



