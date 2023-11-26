```cpp
int add(int a, int b, int c = 0) {  
    return a + b;  
} 
```
---
We can combine [[02_Function Overloading|overloaded function]] with the help of default arguments like this:

```cpp
#include <iostream>  
  
using namespace std;  
  
int add(int a, int b) {  
    return a + b;  
}  
  
int add(int a, int b, int c ) {  
    return a + b + c;  
}  
  
int main() {  
    cout <<  add(1, 2) << endl;  
    cout << add(2, 5, 9);  
}
```

##### Instead of this we can write:
```cpp
#include <iostream>  
  
using namespace std;  

  
int add(int a, int b, int c = 0 ) {  
    return a + b + c;  
}  
  
int main() {  
    cout <<  add(1, 2) << endl;//Here the value of c = 0 if not stated otherwise.
    cout << add(2, 5, 9);//Value of c is 9.  
}
```