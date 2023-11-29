```cpp
#include <iostream>  
using namespace std;  
  
class Shape {  //Generalization and abstract class
public:  
    virtual bool isCircle(){};  //Not required
    virtual bool isRectangle(){};  //Not required
    virtual float perimeter() = 0;  //Required
    virtual float area() = 0;  //Required
};  
  
class Circle : public Shape {  
private:  
    const float PI = 22.0 / 7.0;  
    float radius;  
  
public:  
    Circle(float radius = 0) {  
        this->radius = radius;  
    }  
  
    float perimeter() override {  
        return 2 * PI * radius;  
    }  
  
    float area() override {  
        return PI * radius * radius;  
    }  
  
    bool isCircle() override {  
        return true;  
    }  
};  
  
class Rectangle : public Shape {  
private:  
    float length;  
    float breadth;  
  
public:  
    Rectangle(float length = 0, float breadth = 0) {  
        this->length = length;  
        this->breadth = breadth;  
    }  
  
    float perimeter() override {  
        return 2 * (length + breadth);  
    }  
  
    float area() override {  
        return length * breadth;  
    }  
  
    bool isRectangle() override {  
        return true;  
    }  
};  
int main() {  
    Shape *shape = new Rectangle(2, 5);  
    cout << shape->area() << endl;  
  
    shape = new Circle(5);  
    cout << shape->area();  
    return 0;  
}
```