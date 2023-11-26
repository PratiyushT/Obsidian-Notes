To access members using variable name we use dot `.` operator. 

To access members using pointer, we use arrow `->` operator. This arrow is a  
de-referencing operator.

```cpp
int main() {  
	*pointer = new Rectangle();  
    Rectangle variable_name{};  
    variable_name.setLength(55);  
    pointer->setLength(12);  
    cout << pointer->getLength();  
    cout << variable_name.getLength();  
    return 0;  
}
```
