A function calling itself is called recursion.


```cpp
#include <iostream>  
  
using namespace std;  
  
int x = 10;  
  
int factorial_recursion(int n) {  
    if (n == 1) return n; //Base condition  
  
    return n * factorial_recursion(n - 1); //Recursive condition  
}  
  
int main() {  
    cout << factorial_recursion(5);  
}
```


If base condition is not properly return, it might crash the program with and endless loop.