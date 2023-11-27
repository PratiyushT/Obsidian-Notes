Those functions that expand in the same line they are called are called inline functions. There is no separate block of memory for these functions like [[03_Allocation of Memory for Functions|normal functions]] in the code section. They are bundled with main function every time they are called.. 

## How to make functions inline:

1. [[06_Parameter Passing#Pass by Reference|Pass by reference]]
2. Write the keyword `inline` in front of a function
3. [[09_Scope Resolution Operator|Define a function inside a class]]
4. Using the `inline` keyword

```cpp
inline add(int a, int b){
	return a + b;
}
```