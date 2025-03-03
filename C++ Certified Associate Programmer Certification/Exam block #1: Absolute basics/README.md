# 1. Machine and High-Level Programming Languages
#### What is a Machine Language?
Machine language is a set of binary instructions (0s and 1s) that a computer's CPU understands directly. Each instruction corresponds to a specific operation, such as addition, subtraction, or data movement.

**Example of Machine Code (in Binary)**
```
10111001 00000001
11000011 00000100

```
- These sequences of bits correspond to CPU instructions.

#### Challenges of Machine Language
- **Difficult to read and write:** Only 0s and 1s, making programming extremely difficult.
- **Hardware-dependent:** Different CPUs have different instruction sets.

#### What is an Assembly Language?
To make programming easier, Assembly Language was introduced. It uses human-readable mnemonics instead of binary code.

**Example of Assembly Code**
```
MOV AL, 1
ADD AL, 2

```
- MOV AL, 1 → Moves value 1 into register AL
- ADD AL, 2 → Adds 2 to the value in AL

#### Challenges of Assembly Language
- Still hardware-dependent.
- Requires knowledge of CPU architecture.
- Difficult to debug compared to high-level languages.

### High-Level Programming Languages
To overcome the limitations of machine and assembly languages, high-level languages (HLLs) like C, C++, Java, and Python were developed.

#### Characteristics of High-Level Languages
- ✅ Easier to read and write.
- ✅ Machine-independent (portable across different processors).
- ✅ Uses natural language-like syntax.
- ✅ Provides abstraction from hardware details.

**Example of High-Level Code (C++)**
```cpp
#include <iostream>
using namespace std;

int main(){
cout << "Hello Mithun Dama!" << endl;

return 0;
}

```

# 2. Compilation Process
The compilation process converts human-readable high-level code into machine code.

#### Steps of Compilation
- Preprocessing (#include, #define handling)
- Compilation (Syntax checking, conversion to assembly)
- Assembly (Converting assembly to machine code)
- Linking (Combining multiple object files, linking libraries)
- Execution (Running the compiled executable)

