```cpp
#include <iostream>  
#include <string>  
  
using namespace std;  
  
class Rectangle {  
private:  
    float length;  
    float breadth;  
public:  
    void setLength(float l) { //Mutator 
        length = l < 0 ? length = 0 : length = l;  
    }  
  
    float getLength() { //Accesssor
        return length;  
    }  
  
    void setBreadth(float b) {  
        breadth = b < 0 ? breadth = 0 : breadth = b;  
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
    Rectangle *rect1 = new Rectangle();  
    rect1->setLength(-1);  
    cout << rect1->getLength();//0
    return 0;  
}
```

