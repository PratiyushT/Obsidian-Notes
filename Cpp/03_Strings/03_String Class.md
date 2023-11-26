### Functioning: 
This creates an array of characters heap with the delimiter. 

The array that is created is bigger than the user given string to accommodate future changes as array once declared cannot be changed in size. If the user input is later to be changed and the string is bigger than the created array, the previous string(the char array) is _deleted and new one is created else, the change is reflected in old array. Memory is allocated at heap not stack.

```cpp
#include <iostream>  
  
using namespace std;  
  
int main() {  
    string s;  
    string a = "Hello";  
    cout << a.length();  
}
```
### Methods:
    
    1. str.length(); //len of string
    2. str.capacity(); //len of array created which is the capacity of the string.
    3. str.resize(size); //change the capacity. Capacity will be >= size
    4. str.max_size(); //Give max size of allowed characters in the used compiler.
    5. str.clear(); //Clears the string i.e. empty string 
    6. str.empty(); //True if empty string else false. and sooo..................on........