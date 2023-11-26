By default, **all class variables and functions are private**, i.e., they can only be modified or accessed within the class definition itself. This is a form of [[05_OOPS/01_Introduction#Principles of OOPS|encapsulation.]]

**However, we can use `public:` keyword to make them accessible outside the class.

Data hiding means hiding data from parts of the program that don’t need to access it. More specifically, one class’s data is hidden from other classes. Data hiding is designed to protect well-intentioned programmers from honest mistakes. Programmers who really want to can figure out a way to access private data, but they will find it hard to do so by accident

---
#### Wrong code (in this context)
```cpp
#include <iostream>  
#include <string>  
  
using namespace std;  
  
class Rectangle {  
  
    float length;  
    float breadth;  
  
    float area() {  
        return length * breadth;  
    }  
  
    float perimeter() {  
        return 2 * (length + breadth);  
    }  
};  
  
int main() {  
    Rectangle circle, rectangle;  
    circle.length = 12; //Erorr => ‘float Rectangle::length’ is private within this context  
    return 0;  
}
```

---
#### Correct Code (But not good code)
```cpp
#include <iostream>  
#include <string>  
  
using namespace std;  
  
class Rectangle {  
public:  
    float length;  
    float breadth;  
  
    float area() {  
        return length * breadth;  
    }  
  
    float perimeter() {  
        return 2 * (length + breadth);  
    }  
};  
  
int main() {  
    Rectangle circle, rectangle;  
    circle.length = 12;  
    rectangle.length = 15.5;
    cout << circle.length << endl;  //12
    cout << rectangle.length << endl; //15.5
    return 0;  
}
```

---

## Data is private, function is public

