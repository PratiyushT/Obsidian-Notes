[[02_Parent Class Constructor| In Constructors]]: First base then derived.  
  
In Destructors: First derived then base.  
  
```cpp
class Test {  
public:  
    Test() {  
        int x = 10;  
        cout << "This is executed at beginning" << endl;  
    }  
 ~Test() {//Cannot be overloaded.  
        delete x; //Definitions in constructor should always be del.  
        cout << "This is executed at the end when memory is cleared";  
    }  
};  
   
int main() {  
    Test stack;//Automatic  
    Test *heap = new Test;//We have to delete manually.  
    delete heap;//Destructor will run;  
    return 0;  
}
```