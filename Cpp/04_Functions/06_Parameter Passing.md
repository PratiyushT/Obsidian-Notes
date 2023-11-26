
### What are the methods for a function to take or pass parameters?

1. **Pass  or Call by Value**
2. **Pass or Call by Address**
3. **Pass or Call by Reference**
---
## Pass by Value
```cpp
void swap(int a, int b) {  //a & b are formal paramters or parameters
    int temp;  
    temp = a;  
    a = b;  
    b = temp;  
}  
  
int main() {  
    int x = 12;  
    int y = 8;  
  
    swap(x, y);  
     cout << x << " " << y; // 12 8  
    //x & y are actual parameters or arguments
    //The value is still 12 and 8. After activation record of swap function  
	//is deleted, the local variables of the function are also deleted.         //Hence, swapping is done inside the function and not on actual arguments.  
  
}```

Here we are passing the data value of `x` and `y`. Hence, when we change value of `a` and `b` parameters, arguments are not affected after function ends.

---

## Pass by Address

```cpp
void swap(int *a, int *b) {   
//Here we are not reffering to the value of arguments (formal parameters)  
    //we are passing the memory location    int temp;  
    temp = *a;  
    *a = *b;  
    *b = temp;  
}  
  
int main() {  
    int x = 12;  
    int y = 8;  
  
    swap(&x, &y); //Arguments or actual parameters 
    cout << x << " " << y; // 8 12  
}
```

Let's say `x` is at memory location 200 and `y` at 201. Here, we are passing the value of the memory location and not the value of `x` & `y` i.e. `a` and `b` are pointers and no data value. Due to the change in memory location itself, we are changing the arguments as well.

---

## Pass by Reference
Unlike normal function, the [[03_Allocation of Memory for Functions|allocation of memory ]]here is different. When passed by reference, the function is not treated separately. The machine code for the function is bundled along with the `main` function. This is called **inline function**. 

Hence, beyond all the abstraction, there is no actual different function. There is no separate activation record for the `swap` function. Everything is bundled together with the `main` function. So, there are no arguments or parameters. Just normal variables for `main` function. Meaning arguments are same as parameters. They are just aliases for parameters. This meets the concept of [[07_Reference|references]].

```cpp
void swap(int &a, int &b) {  
    //a and b are included in the activation record of main function  
    //Hence, a and b are actually just x and y.    
    //This meets the concept of reference.   
     //Meaning a and b are just alias for x and y.    int temp;  
    temp = a; 
    a = b;  
    b = temp;  
}  
  
int main() {  
    int x = 12;  
    int y = 8;  
  
    swap(x, y);  
    cout << x << " " << y; // 8 12  
}
```


**So, complex logic like loops should be avoided if possible as compiler may automatically make it call by value.**