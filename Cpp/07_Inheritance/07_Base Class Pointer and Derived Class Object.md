If a Base Class pointer is pointing on derived class object then using the base class pointer we can access only inherited methods (methods defined in base class) on derived class object i.e. variable is based on the pointer not the address of the object.


```cpp
class Base {
public:
    void print() {
        cout << "This is base class";
    }
};

class Derived : public Base {
public:
    void func1() {};
};

int main() {
    Base *b;
    // Here we have a pointer for Base class
    b = new Derived();
    //Now, we have derived class assigned to it.
    b->print();
    //We can call public members of base class only not of derived class.
    b->funct1(); //Will result in an error.
    return 0;
}
```


**This is allowed because methods of Base class are 'available' in Derived class.  However we cannot do this because methods of Derived class are not available in Base class.**

```cpp
Derived *d;
b = new Base();//Not allowed because of reason mentioned above.
```

To resolve this we use [[01_Virtual Functions|Virtual Functions]]. 