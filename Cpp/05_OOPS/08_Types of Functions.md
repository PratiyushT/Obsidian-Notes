1. [[06_Constructors|Constructor]]: Called upon object creation
2. Setter/ Mutator: Modify a data member
3. Getter/ Accessor: Modify a data member 
4. Facilitator: Actual functions that do something
5. Inquirer/ Inspector: Checks if object satisfies some condition
6. Destructor: Releases resources used by the class.

A class generally should contain all these types of functions.

```cpp
class Class_Name {  
private:  
    int i1{};  
    int i2{};  
public:  
    Class_Name(int i1 = 0, int i2 = 0) {}  
    //Constructor
    int getLength() {}  
    //Accessor or getter method
    void setLength() {}  
    //Mutator or setter method    
    int doSomething() {}  
    //Facilitator  
    bool isSquare() {}  
    //Inspector or inquiry method     
    ~Class_Name() {}  
    //Destructor  
};
```