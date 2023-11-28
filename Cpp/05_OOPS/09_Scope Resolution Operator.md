**Note: Function signature must match.**

`::` is the scope resolution operator

---
**Why do this?**
Machine code for all functions in a class is stored in code section inside `main `function as [[11_Inline Functions|inline functions]]. For example `subtract` here will be a part of `main` function. 

However, if we write a scope resolution, the machine code for the `add` function is generated separately, i.e., they will be non-inline functions. 

---
**Bottom line:** Using scope resolution => not inline, not using scope resolution => inline function.

---
```cpp
class Name {  
private:  
    int i1 = 1;  
    int i2 = 2;  
public:  
    int subtract(int a, int b) {  
        return a - b;  
    }  
  
    int add(int i3); //This must be here.  
};  
  
int Name::add(int i3) {  
    //Facilitator declared outside 
    //the class using Name::(scope resolution)  
    return i1 + i2 + i3;  
}  
  
int main() {  
    Name val;  
    cout << val.add(3);  
    return 0;  
}
```