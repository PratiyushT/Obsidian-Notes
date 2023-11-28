
A class can either be derived or the object of that class can be used. These are two ways to use a class.

```cpp
class Rectangle {  
    int length;  
    int breadth;  
};  
  
//Cuboid 'isA' Rectangle(Inheritance)  
class Cuboid : Rectangle {  
};  
  
//Table 'hasA' Rectangle.(Use of object of class)  
class Table{  
    Rectangle rect;  
};
```