If a Derived class has not defined a overriding function for a pure virtual function, we get an error. Kind of like `override`.

The sole purpose of pure virtual functions are to achieve polymorphism by creating [[05_Abstract Class|abstract classes]].

---
In the code below, we have commented `sit` in `Dog` class. This means that there is no `sit` method there. Hence, we will get an error at the line where `//Error` is written. 

However, defining `speak` is not as necessary because it is not a ==pure== virtual function. As shown by commenting in `Cat` class.

```cpp
  
#include <iostream>  
using namespace std;  
  
class Animal {  
public:  
    virtual void speak(){};  
    virtual void sit() = 0;  
};  
  
class Dog : public Animal {  
public:  
    void speak() override { cout << "Dog Talks"; }  
    //void sit() override { cout << "Dog Sits"; }  
};  
  
class Cat : public Animal {  
public:  
    //void speak() override { cout << "Cat Talks"; }    
    void sit() override { cout << "Cat Sits"; }  
};  
  
  
int main() {  
    Animal *p = new Dog();//Error  
    p->speak();  
    p = new Cat();  
    p->sit();  
    return 0;  
}
```