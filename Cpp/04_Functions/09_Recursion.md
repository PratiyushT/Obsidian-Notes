A function calling itself is called recursion.


```cpp
#include <iostream>  
  
using namespace std;  
  
int x = 10;  
  
int factorial(int n) {  
    if (n == 1) return n; //Base condition  
  
    return n * factorial(n - 1); //Recursive condition  
}  
  
int main() {  
    cout << factorial(5);  
}
```


If base condition is not properly return, it might crash the program with and endless loop.