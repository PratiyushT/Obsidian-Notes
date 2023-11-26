### Sections of Memory

**The section of memory in C++ compiler is as follows:**
	Code section -> Stack -> Heap

A program executes the binaries stored in the code section, i.e., this is where our code is stored. Variable values are stored in stack or heap.

### Difference between Stack and Heap
A C++ program can only access code section and stack. Memory heap cannot be directly accessed. So, if we were to create a  variable at the heap, we would need to access it through the stack with the help of pointers. 

**Important:** Memory is allocated dynamically in heap. ==**This means that, memory is assigned and known at runtime in heap and compile-time in stack.**== Hence, we can create a array with dynamic size.

#### Allocating values in Stack and Heap
```cpp
int main() {  
    int x[] = {1,2,3}; // Created at stack  
    int *p = new int;  //Created at heap  
	//Pointer is required to access the array created  
	// because it is created in heap.  
	cout << p << endl; //Address at heap.  
	*p = 5; //Changing the value at heap  
	cout << *p << endl;  
	cout << p << endl;//Address does not change.  
	delete p; //Releasing the memory at heap. should Always be done.
}
```

#### Deallocation of memory
Memory at heap are not deleted like memory at stack. Hence, they must always be cleared after they are not required. Hence, when the program is huge and we are using a function. If there is some data at heap that is not manually deleted like data at stack, the memory is still occupied even after the program ends. No pointer is pointing toward that data but the memory address is also not free. Hence, there is[[06_Problems with pointer| memory leak issue]]. We can use the keyword `delete` in C++ to release the memory at heap. However, after releasing the memory at heap, we have a pointer not pointing anywhere. Hence, we should create a [[04_Null Pointer|null Pointer]].