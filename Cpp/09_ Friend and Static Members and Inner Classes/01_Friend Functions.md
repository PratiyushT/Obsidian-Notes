A friend function can access private members of a class outside the class declaration. The function signature must be declared with `friend` keyword to enable friend functions.

Look at this code for further clarification. Here, `friend_func` is a friend function and can access the private variable `x`. However in the commented function `func`, it would throw an error.

```cpp
#include <iostream>  
using namespace std;  
  
class Test {   
    int x = 12;  
	friend void friend_func();  
};  
  
//void func() {  
//    Test t;  
//    cout << t.x << endl;   //Error: int Test::x is private within this context  
//}  
  
void friend_func() {  
    Test t;  
    cout << t.x << endl;  
}  
  
int main() {  
    friend_func();  
    return 0;  
}
```