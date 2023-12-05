[[04_Function Templates|Templates]] are generic data types.

When using class name and template the following is necessary everywhere (Definition, declaration, initialization):
`ClassName<datatype>`
```cpp
  
template<class T>//Function template
void display(T value) {  
    cout << value;  
}  
  
template<class T>  //Class Template
class Try {  
    T value;  
public:  
    void print(T);  
};  
  
template<class G>  
void Try<G>::print(G value) {  
    cout << value;  
}  
  
int main() {  
    display(22);  
    display('s');  
  
    Try<int> val;  
  
    val.print(12);  
    val.print('s');  
  
    return 0;  
}
```