**Global variables**:  Remain in memory(small space in code section) as long as program runs. Accessible by all functions.

---
**Local variable**: Terminated from memory when the function it is initialized in is terminated. Accessible within the scope of its block.

---
**Static Variable**: **_Accessible only within the scope of its block. Remains in memory like global variable. i.e. it is created only once no matter how many times the function is called.

It means that the variable has lifetime of global variable but is bounded to its scope.

```cpp
#include <iostream>  
  
using namespace std;  
  
int x = 10;  
  
void func() {
    static int counter_static = 0;  
    ++counter_static;  
    cout << "This function was called: " << counter_static << endl;  
}  
  
int main() {  
    func();  
    func();  
    func();  
    func();  
    //However unlike global variable, we cannot access it outside its scope  
    //v = 11; //Not allowed    return 0;  
}  
  
//Output  
//This function was called: 1  
//This function was called: 2  
//This function was called: 3  
//This function was called: 4
```