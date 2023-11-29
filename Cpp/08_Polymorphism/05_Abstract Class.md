Abstract classes are the classes containing at least one virtual function.

---
We cannot create an object of abstract class. But we can create a pointer of that.
![[Pasted image 20231128174650.png]]

```cpp
class Animal {  //This is an abstract class
public:  
    virtual void speak(){};  
    virtual void sit() = 0;  
};  
  
class Dog : public Animal {  
public:  
    void speak() override { cout << "Dog Talks"; }  
    void sit() override { cout << "Dog Sits"; }  
};

int main() {  
    Animal not_allowed;//Error
    Animal *not_allowed_also = new Animal();//Error  
    Animal *allowed = new Dog();//No Error  
}
```
---
## Purpose or categorization of classes with inheritance

1. **All concrete functions in base:** Re-usability
    
2. **Some concrete and some virtual function:** Polymorphism and Re-usability
    
3. **All virtual functions:** Polymorphism -> *This is also called as an interface.*
![[Pasted image 20231128175214.png]]