A static member of a class belongs to the class itself and not an instance of a class.

That is even though many objects of the same class, memory is allocated only once.

Static member functions cannot access non-static data members of a class.

![[Pasted image 20231129084059.png]]

```cpp
#include <iostream>  
using namespace std;  
  
class Test {  
public:  
    static int count;  
    static int counter() {  
        ++count;  
        return count;  
    }  
};  
  
int Test::count = 0;  
int main() {  
    Test t;
    Test t2;  
    cout << t.counter()<<endl;//Out: 1  
    cout << Test::counter()<<endl;//Out: 2  
    cout << t2.counter();//Out: 3
  
    return 0;  
}
```