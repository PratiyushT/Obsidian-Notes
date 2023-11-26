
In C++, `array[0] = array` i.e. array always[[02_Pointers and Reference/01_Introduction| points]] to the first element.  
```cpp
int main(){  
    int a[12]={1,2,3,4};  
    cout << *a; //Array is a pointer so we have to dereference it in this case.  
}
//Output: 1
```
5. During compile time, `arr[i] = *(arr + i)` which means, `arr[i]` is just better way of dereferencing the array. [[05_Pointer Arithmetic|Note that we are not moving the pointer a while doing either of this.]]
```cpp
int main(){  
    int a[12]={1,2,3,4};  
    cout << a[2] << endl; //Access second element of array a.  
    cout << *(a + 2); // Access second element from memory location a  
    // i.e. access second element of array.}
```

---
