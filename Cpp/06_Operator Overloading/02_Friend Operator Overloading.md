A friend function is written outside a class. However, the function signature must be defined inside the class with the keyword `friend` in front of it. We do not use [[09_Scope Resolution Operator|scope resolutions]] with them. 

---
### Features
1. They are global functions.
2. They have access to private members of a class they are defined in.

Here, lets say Ray and Sam are two friends. They want to add money but do not know arithmetic. So they call the help of a third friend. He helps them add the money and returns the added value. This is the concept of friend functions.


```cpp
class Complex {  
private:  
    int real;  
    int imaginary;  
  
public:  
    Complex(int real = 0, int imaginary = 0) {  
        this->real = real;  
        this->imaginary = imaginary;  
    }  
  
    friend Complex operator+(Complex c1, Complex c2);  
  
    void display() {  
        string oper = this->imaginary > 0 ? " + " : " - ";  
        cout << this->real << oper  
             << abs(this->imaginary)  
             << "i";  
    }  
};  
//Written outside class
Complex operator+(Complex c1, Complex c2) {  
    Complex value(c1.real + c2.real,  
                  c1.imaginary + c2.imaginary);  
    return value;  
}  
  
  
int main() {  
    Complex c1(1, -2);  
    Complex c2(3, 5);  
    Complex c3 = c1 + c2;  
    c3.display();  
}
```