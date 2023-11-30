```cpp
#include <iostream>  
using namespace std;  
  
int main() {  
    int a = 1;  
    int b = 2;  
    try {  
        cout << a << endl;  
        if (b == 2) throw b;  
        //When throw is encountered, flow goes to catch block.  
    } catch (int e) {  
        cerr << "B = " << e;  
    }  
    return 0;  
}
```

![[Pasted image 20231129220925.png]]