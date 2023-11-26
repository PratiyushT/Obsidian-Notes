### Types of Values
- **Scalar Values**: ` x = 5` i.e. has only magnitude
- **Vector/ List**: `Arr = (5,6,7,8)` i.e. has magnitude and direction .

***
### Features of Array
```cpp
//dataype array_name[size] 
int a[11] = {1,2,3}; // Declaring and Initializing an array
//The rest of the value i.e. from index 3 all values are 0.
```

1. An array acts as a [[02_Array as a pointer|pointer]] to its first element i.e. it has memory location of the first element saved to its variable and not its value.
2. When arrays are declared in this way, their size is constant i.e. the size cannot be changed for the same array]]. [[03_Stack, Heap and Pointers#Difference between Stack and Heap|However we can create a dynamic array.]]
3. It stores data in contiguous location in memory, i.e., ==side by side.==
4. For example, if the first element is located at memory location 200, next will be at 204 (int takes 4 bytes of data) and 208 and so on. 
---
