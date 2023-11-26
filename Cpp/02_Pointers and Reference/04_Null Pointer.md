When pointer is not pointing anywhere, it is a null pointer. We can assign a null pointer by the keyword `nullptr`.  We need to do this to prevent the misuse of memory allocation. If we do not point to a null, we could possibly assign a value to a location we do not want causing issues.

######  Improper Code
```cpp
int main() {  
    int *p = new int;  
	*p = 5;
    p = nullptr;  
    //Never do this before deleting the value.    
    //If we do this, we lose access to the value at heap 
    //Hence we should always point to null only after de-allocation.    
    delete p; //No point in freeing this memory now. as nothing is located here  
    cout << p << endl; //Pointer is pointing to deallocated memory  
```
###### Proper code
```cpp
int main() {  
    int *p = new int;  
    *p = 5;  
    delete p;     
    p = nullptr;  
    cout << p << endl; // Output: 0  
}
```

###### Proper code for Dynamic use
 ```cpp
 int main() {  
    int *p = new int[3];  
    delete[] p; //Always delete before new data values.  
    p = new int[10];  
    delete[] p;  
    p = nullptr;  
    cout << p;  
}
```