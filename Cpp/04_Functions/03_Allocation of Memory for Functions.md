In the [[03_Stack, Heap and Pointers|code section of the memory]], there will be **machine** code for our main function and all other functions as these are various pieces of code unless [[06_Parameter Passing#Pass by Reference|called by reference]]. This means that even though a function is not called, it will still occupy space in the memory. For example:

```cpp
#include <iostream>  
  
using namespace std;  
  
int add(int a, int b) { //Stored in the code section  
	int random_variable;
    return a + b;  
}  
  
int subtract(int a, int b) { //Stored in the code section  
    return a - b;  
}  
  
int main() { //Stored in the code section 
	int a, b, c;
    int added_value = add(1, 2);//Stored in stack  
    cout << added_value;  
}
```

The machine code for `add` and `subtract` functions are not copied when it is called inside the main function. Instead, it is treated as a separate piece of code and is kept in the code section as such i.e. there will be three different pieces of code in this example. 

---
## Activation Record of a function

Now, in the example above, when main function is called, memory is allocated for variable  `a`, `b`, `c` and `added_value` (in this case in the stack). It means that 16 bytes in total is allocated for these 4 variables. This means that these memory locations are associated with the main function. This is the activation record of the `main` function. It is deleted when main function terminates. 

Similarly, int the `add` function, we have declared a `random_value` variable which will be allocated int he stack memory and it is associated with the `add` function when called. This is the activation value of the `add` function. The return value is then copied in the `added_value` variable in the `main` function. After this the activation record is deleted. [[03_Stack, Heap and Pointers#Deallocation of memory|However, when the memory is allocated in the heap, it is not deleted automatically.]]

The activation record is fresh for every call. Meaning that for each call of a function memory for the variables is created freshly in the stack.
