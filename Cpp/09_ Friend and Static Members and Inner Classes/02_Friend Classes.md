Classes can also be treated as friend classes like [[01_Friend Functions|functions]].

```cpp
#include <iostream>  
using namespace std;  
  
class Test {  
private:  
    int x = 12;  
    friend class Test2;  
};  
  
class Test2 {  
    Test t1;  
public:  
    int t2 = t1.x;  //Private memeber of class
};  
  
int main() {  
    Test2 t;  
    cout << t.t2;  
    return 0;  
}
```