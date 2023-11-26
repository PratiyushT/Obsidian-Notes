
```cpp
int main(){  
    int a[3]={1,2};  
    for (int x : a){ // For each int x in array a.  
    //Note that x is a copy not a reference to the memory location.
        cout << x << " ";  
    }  
    //Output: 1 2 0  
}
```

We need to use reference to actually change the element of any array in for each loop.

```cpp
int main() {  
    int a[3] = {1, 2};  
    for (int &x: a) { // For each int x in a.  
        ++x; //Now there is actual change in array element.  
    }  
    cout << a[1];  
    //Output: 3  
}
```

[[05_2-dimensional Arrays or matrices#Looping / Matrix calculation| 2D arrays requires a nested looping approach]] **and using for each loop results in an error**. 
