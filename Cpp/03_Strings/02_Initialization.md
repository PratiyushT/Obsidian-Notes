1. Using [[01_Arrays/01_Introduction|character array]]:
```cpp
int main() {  
    char x[] = "Hello";  
    cout << x << endl; //Hello  
  
    char y[] = {'H', 'e', 'l', 'l', 'o', '\0'}; //Hello  
    cout << y << endl;  
  
    //No string delimiter  
    char z[] = {'H', 'e', 'l', 'l', 'o'};//HelloHello  
    cout << z << endl;  
  
}
```

2.  Using a pointer
```cpp
int main() {  
    char *string_name = "Hello"; //Not supported in C++ 11.  
  
    //This will create a string in heap    
    cout << string_name;  
}
```

3. Using cstring class:
```cpp
#include <iostream>  
#include <cstring>  
  
int main() {  
	//Provides methods like length and so on.
    std::string a = "Hello";  
    std::cout << a.length();  
}
```
