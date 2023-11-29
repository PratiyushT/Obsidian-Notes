Here, `p` is determined at runtime. 

```cpp
#include <iostream>  
using namespace std;  
  
class Animal {//Example of Generalization  
public:  
    virtual void speak() = 0;
    //This is pure virtual class
    //They are abstract meaning they must be overridden
    //By all instances of the class.
    virtual void sit() = 0;
};  
  
class Dog : public Animal {  
public:  
    void speak() override { cout << "Dog Talks"; }  
    void sit() override { cout << "Dog Sits"; }  
};  
  
class Cat : public Animal {  
public:  
    void speak() override { cout << "Cat Talks"; }  
    void sit() override { cout << "Cat Sits"; }  
};  
  
  
int main() {  
    Animal *p = new Dog();  
    p->sit();  
    p = new Cat();  
    p->sit();
    return 0;  
}
```