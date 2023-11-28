While using inheritance, it is important to remember that the ==**default**==constructor of parents class is always executed first. Lets look at this example.

The output is:
```
This is parent constructor default
This is value constructor default
This is parent constructor default
This is value constructor with value 11
```

```cpp
#include <iostream>  
using namespace std;  
  
class Parent {  
    int value;  
  
public:  
    Parent() {  
        cout << "This is parent constructor default" << endl;  
    }  
    Parent(int value) {  
        cout << "This is parent constructor with value " 
        << value 
        << endl;  
    }  
};  
  
class Child : Parent {  
  
public:  
    Child() {  
        cout << "This is value constructor default" << endl;  
    }  
    Child(int value) {  
        cout << "This is value constructor with value " 
        << value 
        << endl;  
    }  
};  
  
int main() {  
    Child child;  
    Child child2(11);  
    return 0;  
}```

#### Calling parameterized constructor of parent class
Instead of default we can call the parameterized constructor of parent.  We can basically send the value to parent class's constructor by this syntax:
```cpp
//Child class parametrized constructor
Child(int value, int valueParent):Parent(valueParent) {  
    cout << "This is value constructor with value "
     << value 
     << endl;  
}
```

Output
```
This is parent constructor default
This is value constructor default
This is parent constructor with value 12
This is value constructor with value 11
```