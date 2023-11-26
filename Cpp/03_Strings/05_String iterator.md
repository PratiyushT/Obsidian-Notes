```cpp
int main() {  
    string s;  
    string a = "Hello";  
    for (string::iterator it = a.begin(); it != a.end(); ++it) {  
        cout << *it;  
    }  
}
```

We can also use [[03_Looping in Array|array loop]].