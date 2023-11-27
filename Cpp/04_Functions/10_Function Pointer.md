Syntax: `datatype (*pointer_name)(argument_list);`

A function pointer can point to any function as long as the function signature (only data types and not names) matches.

```cpp
#include <iostream>  
  
using namespace std;  
  
int max(int x, int y) {  
    return x > y ? x : y;  
}  
  
int min(int x, int y) {  
    return x < y ? x : y;  
}  
  
int main() {  
    int (*fp)(int x, int y);  
    fp = max;  
    (*fp)(1, 5); //Max function is called  
    fp = min;  
    (*fp)(11, 100);//Min is called  
  
}
```