When we buy a car, we do not want a garbage value like a random color. We want to a color of our choice.

Likewise, when we **initialize an object**, we do not want garbage value but certain values (like length and breadth).

Hence we use **constructors**.

---
**Types of constructors:**

1. Default constructor
    
2. Parametrized constructor
    
3. Non-parametrized constructor
    
4. Copy constructor: We are taking a reference here to avoid creation of a new rectangle when we just want the value to copy, i.e., if we do not use reference we will create a new rectangle object.
---

```cpp
#include <iostream>  
#include <string>  
  
using namespace std;  
  
class Rectangle {  
private:  
    float length;  
    float breadth;  
public:  
    Rectangle() {// Non-parameterized constructor  
        setLength(0);  
        setBreadth(0);  
    }  
  
    Rectangle(float l, float b) { //Parameterized constructor  
        setLength(l);  
        setBreadth(b);  
    }  
  
    Rectangle(Rectangle &rect) { //Copy constructor  
        setLength(rect.length);  
        setBreadth(rect.breadth);  
    }  
  
    void setLength(float l) {  
        length = l < 0 ? length = 0 : length = l;  
    }  
  
    float getLength() {  
        return length;  
    }  
  
    void setBreadth(float b) {  
        breadth = b;  
    }  
  
    float getBreadth() {  
        return breadth;  
    }  
  
    float area() {  
        return length * breadth;  
    }  
  
    float perimeter() {  
        return 2 * (length + breadth);  
    }  
};  
  
int main() {  
    Rectangle *rect1 = new Rectangle(12, 5);  
    Rectangle rect1_copy = Rectangle(*rect1);  
    cout << rect1_copy.getLength();  
    return 0;  
}
```

These are [[02_Function Overloading|overloaded constructors (functions)]].