We can write a `throw` statement in a function to catch an error. Then define `catch` block in another function. This way program will crash safely without returning a bogus value.

```cpp
#include <iostream>  
using namespace std;  
  
float division(int x, int y) {  
    if (y == 0) {  
        throw 1;  //No return just throw.
    } else {  
        return float(x) / float(y);  
    }  
}  
  
int main() {  
    try {  
        division(1, 0);  
    } catch (int e) {  
        cerr << "Division by zero Error: " << e;  
    }  
    return 0;  
}  
//Output;
//Division by zero Error: 1
```