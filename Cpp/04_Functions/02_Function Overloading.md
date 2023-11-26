The header of a function is called as signature or prototype.

---
Writing function with same name but different argument list is called function overloading. Return type does not matter when we overload functions as shown in the commented portion of code below.

For example, `add` is overloaded function.

```cpp
#include <iostream>  
  
using namespace std;  
  
int add(int a, int b) {  
    return a + b;  
}  

//This is not allowed as only the return type is 
//different parameter list is same.
//double add(int a, int b) {  
//    return a + b;  
//} 

double add(double a, double b) {  
    return a + b;  
}  
  
int add(int a, int b, int c) {  
    return a + b + c;  
}  
  
int main() {  
    int two_sum = add(1, 2);  
    int three_sum = add(1, 2, 3);  
    double double_sum = add(1.0, 2.3);  
    cout << two_sum << " " << three_sum << endl;//Output: 3 6  
    cout << double_sum; // Output:3.3  
}
```

