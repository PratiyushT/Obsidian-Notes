Reference is just an alias for another variable i.e. the name is different memory location is same.

It should always be initialized and cannot be just declared. 

References do not consume any memory at all.

We cannot change the value of reference.

```cpp
int main() {  
	int a = 11;
    int x = 10;  
    int &y = x;  
//	&y = a;       THis is not allowed
//error: lvalue required as left operand of assignment
    cout << y << endl; // 10  
    ++y;  
    cout << x; //11  
}
```
---
### Reference to a pointer
```cpp
int main() {  
    int x = 10;  
    int *y = &x;  
    int *&z = y; // This is a reference to a pointer.  
    //As y is a pointer we have to do this to create a reference.  
    cout << z << endl; // Output: Some memory address  
    cout << *z; //Output: 10  
}
```
----
### R-value and L-value
R-value (Data value): `a = x;` value of variable x is stored in variable a.
L-value (Address): `x = 10;` data literal is stored in variable x.

So, when **==x is use as R-value it is data and L-value it is address==**

----
