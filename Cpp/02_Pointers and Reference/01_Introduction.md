A pointer is basically an address to a data value.
### Types of variable:

1. Data variable: `int x = 10`
2. Address variable: `int *p` with the asterisk (`*`) we are making this a pointer. It does not store a value. ==It stores address or memory location of a value.==  The `&` sign is used for memory address of a variable.

For example: 
```cpp
int main() {  
    int x = 10;  
    int *p = &x;  //Pointer is saving the address of x.
    cout << p << endl;//Output is Something like 0x13c29ffc74 is the output 
    cout << &x << endl; //The value is same as p. i.e. the output is as above. 
    cout << *p << endl; // This is dereferencing.
    //Output is the value of x i.e. 10  
}
```

---
### Dereferencing
Dereferencing refers to the process of going to the [[02_Use of pointers#Sections of Memory|memory address]] and taking the data value. It is done in C++ with the help of asterisk(`*`) in the right hand value.

```cpp
int *p //We are declaring a pointer here.
p = &some_value; //We are initializing a pointer here.
int the_value_at_locaton = *p; //We are dereferencing here
```

***

