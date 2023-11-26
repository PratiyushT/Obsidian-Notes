![[Screenshot from 2023-11-26 11-36-12.png]]

Here we can see that (in the bottom right portion of the picture) `p` is a pointer to array at heap. So, when we use copy constructor, in the line, `p = t.p` we are pointing to the same array as `t`, . i.e. , `t` and `t2` are pointing to the same memory location. We do not want that. Hence, we can use a deep  copy constructor. Note that deep copy constructors need to be made as per the need. This is not exact for every deep copy constructor.

```cpp 
class Test {  
public:  
    int size;//Just for learning purpose  
    int *ptr;  
  
    Test(int x) {  
        size = x;  
        ptr = new int[size];  
    }  
  
    Test(Test &ref) {  
        size = ref.size;  
        ptr = ref.ptr;  
    }  
};  
  
int main() {  
    Test t1(5);  
    Test t2(t1);  
    t1.ptr[1] = 12;  
    cout << t1.ptr[1] << endl;  
    t2.ptr[1] = 100;  
    cout << t1.ptr[1]; //100  
    //We can see that t2 and t1 are    
    //Pointing to the same array  
    return 0;  
}
```

---

### Correct Program

```cpp
#include <iostream>  
#include <string>  
  
using namespace std;  
  
class Test {  
public:  
    int size;//Just for learning purpose  
    int *ptr;  
  
	Test(int x) {  
	    size = x;  
	    ptr = new int[size];  
	    for (int i = 0; i < size; i++) {  
	        ptr[i] = i;  
	    }  
	}  
	  
	Test(Test &ref) {  
	    size = ref.size;  
	    ptr = new int[size]; 
	    //Create a totally new array at heap.
	    for (int i = 0; i < ref.size; i++) {  
	        ptr[i] = ref.ptr[i];  
	        //Copy all elements also
	    }  
	}
};  
  
int main() {  
    Test t1(5);  
    Test t2(t1);  
    t1.ptr[1] = 12;  
    cout << t1.ptr[1] << endl;  
    t2.ptr[1] = 100;  
    cout << t1.ptr[1]<<endl; //12  
    cout << t2.ptr[1]; //100  
    //We can see that t2 and t1 are now truly independant
    return 0;  
}
```