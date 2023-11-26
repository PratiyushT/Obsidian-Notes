## Return by Address
```cpp
int *arr_of_num(int size) {  
    int *p = new int[size]; //Array created in heap  
    for (int i = 0; i < size; ++i) {  
        p[i] = i;  
    }  
    return p;  
}
```
**Note: We cannot do the same if pointer is pointing to a stack memory location as the memory is deleted automatically as soon as function ends deleting address inside the function also results in same.**

One use case is creating an array at heap and using the returned pointer value or address to access that array.

--- ---
## Return by Reference
[[07_Reference#R-value and L-value|Function is generally used as Left-Hand value. However, this method allows us to use it as Right-Hand value.]]

```cpp 
int &func(int &a) { //Call by reference.  
    return a;//This will not return the value of a. It will return x itself.  
}  
  
int main() {  
    int x = 10;  
    func(x); //Now func(x) will act as x only.  
  
    func(x) = 12; //Function is written in LHS with this method  
//    and the function acts as x itself.  
    cout << x << endl;  
    x = 25;  
    cout << func(x);  
}
```
