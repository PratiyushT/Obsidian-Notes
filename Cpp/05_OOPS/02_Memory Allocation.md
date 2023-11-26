## Storage of classes

Variables consume space. However, functions will not take any space. Hence, in the program below, if the data type of `length` and `breadth` was int, the class `Rectangle` would take 8 bytes.

```cpp
class Rectangle {  
    float length;  
    float breadth;  
  
    float area() {  
        return length * breadth;  
    }  
  
    float perimeter() {  
        return 2 * (length + breadth);  
    }  
};
```

---
