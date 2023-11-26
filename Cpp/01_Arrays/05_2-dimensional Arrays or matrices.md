```cpp
int main() {  
//  float array_name[row][colum];  
    int A[3][4]; //Matrix of order: 3 X 4 
    //Number of elements = row * column* 
    return 0;  
}
```

Although, it looks like a matrix, the data in the computer memory is still laid out in a linear format in a single line. The compiler makes it seem like a matrix. This is just for further clarity and it is not required.

***
#### Initializing the Array

```cpp
int main() {  
	int A[2][3] = {{2, 5, 9},  
	                {6, 9, 15}}; //Matrix of order: 2 X 3
}
```

**OR**

```cpp
int A[2][3] = {2, 5, 9, 6, 9, 15};
```
***
#### Accessing the value

```cpp
int main() {  
//  float array_name[row][colum];  
    int A[2][3] = {2, 5, 9, 6, 9, 15};  
    cout << A[0][2]; //9  
    return 0;  
}
```
***

#### Looping / Matrix calculation

```cpp
int main() {  
    int a[2][3] = {1, 2, 3, 4, 5,11};  
    int b[2][3] = {5, 21, 2, 3, 5,6};  
    int c[2][3];  
	
    for (int i = 0; i < 2; ++i) {  
        for (int j = 0; j < 3; ++j) {  
            
            cout << c[i][j] << " ";  
            if (j == 2) {  
                cout << endl;  
            }  
        }  
    }  
  
}
```

