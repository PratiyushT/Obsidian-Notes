`[[nodiscard]]` is an attribute used before a function to tell the compiler that the return value of that function should not be ignored. For example:
```cpp
[[nodiscard]] int foo() {
    return 42;
}

int main() {
    foo(); 
    // Warning: ignoring return value
    //of function declared with 
    //'nodiscard' attribute
    return 0;
}

```