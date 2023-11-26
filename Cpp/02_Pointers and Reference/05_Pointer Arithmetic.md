### Arithmetic Operations Allowed in Pointers:
1. `p++`
2. `p--`
3. `p += number / p = p + number`
4. `p -= number/ p = p - number`
5. `third_pointer = second_pointer - p`
[[02_Array as a pointer|Note that we are moving the pointer here unlike how array initialization works.]]
### How arithmetic operations work
```cpp
int main() {  
    int a[] = {1001,20,49};  
    int *p = a;  
    p += 2; //Moves by 8 bytes as int size is 4.  
    cout << *p << endl;   //Output: 49
}
```

Here when we use `++p` we are moving by 4 bytes and not 1. This means that when we perform arithmetic operation pointer automatically apply the size. 

For example, here our first element in array a, i.e., 1001. Lets suppose it is at memory location 201-204. So when we perform `p += 2` our pointer automatically points to 209 which is the third element (49) skipping over 205-208 as these 4 bytes are allocated for second element i.e. 20. Similar thing would happen with other data types.

```cpp
void PointerArithmetic(){
    int A[]={2,4,6,8,10,12};
    int *p=A;
    
    // move pointer to next location to print 4
    p += 1;
    cout<<*p;
    
    p=p+3; // pointer will be pointing on 10
    
    cout<<p[-4] ;  // complete this statement to print 2 without moving pointer
}
```
