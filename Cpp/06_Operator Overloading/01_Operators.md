`+`, `*`, `-`, `()`, `++`, `new`, `delete`, etc are some examples of operators in C++.

#### The Operator Overloaded portion
```cpp
Complex operator+(Complex &number) {  
    Complex value;  
    value.real = this->real + number.real;  
    value.imaginary = this->imaginary + number.imaginary;  
    return value;  
}
```

```cpp
Complex c3 = c1.operator+(c2);
Complex c3 = c1 + c2;
//These two have the same meaning when being called in an object
```
---

### The whole program
```cpp
#include <iostream>  
  
using namespace std;  

class Complex {  
private:  
    int real;  
    int imaginary;  
  
public:  
    Complex(int real = 0, int imaginary = 0) {  
        this->real = real;  
        this->imaginary = imaginary;  
    }  
  
    Complex operator+(Complex &number) {  
        Complex value;  
        value.real = this->real + number.real;  
        value.imaginary = this->imaginary + number.imaginary;  
        return value;  
    }  
  
    void display() {  
        string oper = this->imaginary > 0 ? " + " : " - ";  
		cout << this->real << oper   
		     << abs(this->imaginary)   
			 << "i";
    }  
};  
  
  
int main() {  
    Complex c1(1, -2);  
    Complex c2(3, 5);  
    Complex c3 = c1 + c2;  
    c3.display(); //4 + 3i  
}
```