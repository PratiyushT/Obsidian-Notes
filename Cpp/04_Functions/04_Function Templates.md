Functions that are generic in terms of data types are called function templates. A [[05_Default Arguments|default argument]] cannot be a template.

```cpp
template <class T>  
T add(T a, T b) {  
    return a + b;  
}
```
Same as
```cpp
template <typename T>  
T add(T a, T b) {  
    return a + b;  
}
```

---
#### Whole Program
```cpp
#include <iostream>  
  
using namespace std;  
  
template <typename T>  
T add(T a, T b) {  
    return a + b;  
}  
  
int main() {  
    int int_sum = add(1, 2);  
    double double_sum = add(1.11f, 2.21f);  
    cout << int_sum << endl;// Output: 3  
    cout << double_sum; // Output:3.32  
}
```
