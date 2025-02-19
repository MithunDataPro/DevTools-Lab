# Keywords:

## Break:
Break Out Of a Loop.
```cpp
# include <iostream>
using namespace std;

int main() {
    for(int i = 1; i<20; i++){
        cout << i << "\n";
    if (i == 13){
        break;
    }
}
    return 0;
}

```

---

## Continue:

```cpp
# include <iostream>
using namespace std;

int main() {
    for(int i = 1; i<=20; i++){
    if (i == 13){
        continue;
    }
    cout << i << "\n";
}
    return 0;
}

```
