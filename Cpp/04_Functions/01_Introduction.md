### Types of Programming:
1. **Monolithic programming:** No modular approach and the whole program in written as a single unit.
2. **Modular Programming:** Program is split into manageable, functional, reusable pieces of code.

---
### Characteristics of a function:
1. Name: Used to call a function and [[02_Function Overloading|overload ]]a function.
 
2. Parameter/ Argument List (Inputs): Parameters tell us what the function will take, while arguments tell us what their values are. The order of your parameters and arguments matter. If you change the order of them, you need to change them accordingly in both places i.e. parameter in function declaration, argument in function call.

3. Return Type (int, void, etc.): Returns a value to be copied by a variable where it is called. Marks the end of a function. The can only be one return value.

```cpp
returnType function_name(parameter_list){}
```


---

==**Note==:** Avoid using `cin` or `cout` in functions. The function should not have interactivity and should be as independent as possible. 