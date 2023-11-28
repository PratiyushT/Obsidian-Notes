`this` pointer points to the current class. It is a pointer so we cannot use `.`. We have to use the `->` de-referencing. 

```cpp
class Numbers {  
private:  
    int num1;  
    int num2;  
  
public:  
    Numbers(int num1, int num2) {  
        this->num1 = num1;   
        // Here this is pointing to the current class (object)
        //which is object of Numbers class.        
        this->num2 = num2;  
    }  
    int add(int num3) {  
        return this->num1 + this->num2 + num3;  
    }  
};
```