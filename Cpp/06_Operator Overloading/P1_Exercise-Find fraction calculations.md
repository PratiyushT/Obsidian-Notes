```cpp
#include <iostream>  
#include <numeric>  
using namespace std;  
  
class Fraction {  
private:  
    int up;  
    int down;  
  
public:  
    Fraction(int up = 0, int down = 1) {  
        this->up = up;  
        this->down = down;  
    }  
  
    friend Fraction operator+(Fraction f1, Fraction f2);  
    friend Fraction operator-(Fraction f1, Fraction f2);  
    friend Fraction operator*(Fraction f1, Fraction f2);  
    friend ostream &operator<<(ostream &os, Fraction &f);  
    friend istream &operator>>(istream &in, Fraction &f);  
};  
  
Fraction operator+(Fraction f1, Fraction f2) {  
    Fraction added;  
    int factor = lcm(f1.down, f2.down);  
    int req_f1 = factor / f1.down;  
    int req_f2 = factor / f2.down;  
    added.up = (f1.up * req_f1) + (f2.up * req_f2);  
    added.down = factor;  
    return added;  
}  
Fraction operator-(Fraction f1, Fraction f2) {  
    Fraction subtracted;  
    int factor = lcm(f1.down, f2.down);  
    int req_f1 = factor / f1.down;  
    int req_f2 = factor / f2.down;  
    subtracted.up = (f1.up * req_f1) - (f2.up * req_f2);  
    subtracted.down = factor;  
    return subtracted;  
}  
  
Fraction operator*(Fraction f1, Fraction f2) {  
    Fraction value(f1.up * f2.up, f1.down * f2.down);  
    return value;  
}  
  
ostream &operator<<(ostream &os, Fraction &f) {  
    os << f.up << "/" << f.down;  
    return os;  
}  
  
istream &operator>>(istream &in, Fraction &f) {  
    cout << "Enter the numerator: " << endl;  
    in >> f.up;  
    cout << "Enter the denominator: " << endl;  
    in >> f.down;  
    return in;  
}  
  
int main() {  
    Fraction f1;  
    cin >> f1;  
    Fraction f2;  
    cin >> f2;  
    Fraction f3 = f1 + f2;  
    Fraction f4 = f1 - f2;  
    Fraction f5 = f1 * f2;  
    cout << f3 << endl  
         << f4 << endl  
         << f5;  
    return 0;  
}
```

**Note: The program is not entirely correct. But the point was to practice operator overloading.**
