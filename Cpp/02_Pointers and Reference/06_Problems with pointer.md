Problem with pointers may arise during runtime. Hence, they are very dangerous.

## Some problems with pointer
1. **Uninitialized Pointer:** A declared pointer should not be used without initialization.
2. **Memory Leak**: Always deallocate memory after using the `new` keyword i.e.. in heap.  Do not use `nullptr, NULL or 0` without deleting the value in heap.
3. **Dangling Pointers**: When two pointers point to the same address and only one pointer clears that value i.e. uses `nullptr, NULL or 0`, then the other one is a dangling pointer. 

All these problems are caused by programmers negligence. Hence, Java and .Net have removed use of pointers. So, they are called manage languages and are simpler. However, C++ gives full access to the programmer but they must be careful.

