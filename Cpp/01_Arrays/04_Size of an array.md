

The concept behind this is that we divide the length of the whole array by the length of its element. For example, here each element is int and it takes 4 bytes of storage. For the compiler the whole array has 24 bytes. When we divide 24 bytes by the size of its first element, i.e. 4, we get 6. 

==Meaning there are 6 elements with 4 bytes each that span for a total of 24 bytes.==

**Reading the program makes the concept more understandable.**

```cpp
int main() {  
    int arr[] = {1, 2, 30000, 4, 5, 6};  
    int arr_size = sizeof(arr) / sizeof(*arr);  
    // Writing *arr is same as writing arr[0]  
    int arr_size_same = sizeof(arr) / sizeof(arr[0]);  
  
    cout << arr_size << " ";  
    cout << arr_size_same;  
    //Output: 6 6  
}
```

