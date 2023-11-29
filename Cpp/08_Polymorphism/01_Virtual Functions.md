**Virtual functions** make sure that when we call a [[07_Base Class Pointer and Derived Class Object|base class pointer pointing to a derived class object]], the methods of derived class are executed. [[03_Pure Virtual Functions|Pure virtual functions]] also help us create [[05_Abstract Class|abstract classes]].

However only inherited methods (methods defined in base class) can be called like [[07_Base Class Pointer and Derived Class Object|before]]. 

---
This helps us achieve [[02_Runtime Polymorphism|runtime polymorphism]] which means that the correct function to call is determined at runtime based on the type of the object that the function is called on.

```cpp
#include <iostream>  
using namespace std;  
  
class Base {  
public:  
    virtual void display() {  
        cout << "Base class";  
    } 
};  
  
class Derived : public Base {  
public:  
    void display() override{  
        cout << "Derived Class";  
    }  
};  
  
int main() {  
    Base *p = new Derived();  
    p->display();  
    return 0;  
}
```

If we use `override` keyword, there must be a virtual function with the same signature in Base class. This can help prevent errors such as misspelling the function name, changing the parameter list, or forgetting the virtual keyword in the base class.