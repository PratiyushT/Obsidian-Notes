
`Outer::value` and `Outer::public_value` value cannot be accessed inside the inner class without creating an object of it because they are non-static members. However `Outer::static_value` can be as it is a static member.

We can see that after initializing an object, we can also access private data members like `t1.value`.

---
We define inner classes with scope resolution of outer class. `Outer::Inner in;`

---
```cpp
#include <iostream>  
using namespace std;  
  
class Outer {  
    int value = 1;  
    static int static_value;  
  
public:  
    int public_value = 55;  
  
public:  
    class Inner {  
        int x=100;  
  
    public:  
        void show() {  
            cout << x << endl;  
            //cout << value;  
            // We cannot access outer class members like this            //Unless they are static like line below.
            cout << static_value<<endl;  
            Outer t1;  
            //We can create object of outer class  
            //And access all members.            
            cout << t1.public_value<<endl;  
            cout << t1.value<<endl;  
        }  
    };  
    Inner i;
};  
  
int Outer::static_value = 12;  
  
int main() {  
    Outer::Inner in;  
    in.show();  
    return 0;  
}  
  
//Out:  
//100  
//12  
//55  
//1
```