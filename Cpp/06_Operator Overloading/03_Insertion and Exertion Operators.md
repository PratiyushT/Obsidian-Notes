In this code, we used `display` method to display the value of a complex number. However, we can overload the insertion operator `<<` to use it with `cout`.

**Note: They need to be declared as friend function or we will get an error. Also, we need to use references unlike normal operators.**


```cpp
//Take reference of the object (here as num) and reference of an ostream data value (here as os).
ostream &operator<<(ostream &os, Complex num) {  
    string oper = num.imaginary > 0 ? " + " : " - ";  
	ostream &operator<<(ostream &os, Complex num) {  
	string oper = num.imaginary > 0 ? " + " : " - ";  
	os << "(";  
	os << num.real << oper  
	   << abs(num.imaginary)  
	   << "i";  
	os << ")";  
	return os;  
	//Return a reference to ostream
}
```

#### Whole Program 
```cpp
#include <iostream>  
  
using namespace std;  
  
struct Student {  
};  
  
class Complex {  
private:  
    int real;  
    int imaginary;  
  
public:  
    Complex(int real = 0, int imaginary = 0) {  
        this->real = real;  
        this->imaginary = imaginary;  
    }  
  
    friend ostream &operator<<(ostream &os, Complex num);  
  
    friend Complex operator+(Complex c1, Complex c2);  
  
    void display() {  
        string oper = this->imaginary > 0 ? " + " : " - ";  
        cout << this->real << oper  
             << abs(this->imaginary)  
             << "i";  
    }  
};  
  
Complex operator+(Complex c1, Complex c2) {  
    Complex value(c1.real + c2.real,  
                  c1.imaginary + c2.imaginary);  
    return value;  
}  
  
ostream &operator<<(ostream &os, Complex num) {  
    string oper = num.imaginary > 0 ? " + " : " - ";  
    os << "(";  
    os << num.real << oper  
       << abs(num.imaginary)  
       << "i";  
    os << ")";  
    return os;  
}  
  
  
int main() {  
    Complex c1(1, -2);  
    Complex c2(3, 5);  
    Complex c3 = c1 + c2;  
    cout << c1 << " + " << c2 << " = " << c3;  
    //Output: (1 - 2i) + (3 + 5i) = (4 + 3i)
}
```