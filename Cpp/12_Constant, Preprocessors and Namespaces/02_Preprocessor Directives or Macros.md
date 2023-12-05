Happens at pre-compile time i.e. every thing with similar symbol gets replace with the value mentioned before compilation process begins.

```cpp
 #include <iostream>

 #define PI 3.14;
 
 #define SQR(x)(x*x);//Predefine a function.
 
 #ifndef PI//WIll define PI if it is not already defined.
     #define PI 3.14;
 #endif
 
 #define msg(x) #x;//Convert x to string.
 //The # here means that it should be enclosed in double
 //quotes

 using std::cout, std::cin, std::string;

 int main() {
     cout << PI;//Value will be 3.14 before compilation.
     cout << SQR(3);
     cout << msg(Hello)//Hello will be converted to string.
     return 0;
 }
```
