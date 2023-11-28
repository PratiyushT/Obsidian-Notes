`const` is used in methods that guarantee that they do not change a data member of an objects. For example, getter methods.

```cpp
int getLength() const {  
    return length;  
}
//Where length is a data member.
```