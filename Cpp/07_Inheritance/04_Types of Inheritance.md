1. **Simple:** One class inherits from parent. **Rectangle -> Cuboid**
    
2. **Hierarchial:** Multiple class inherits from parent. 
**Shape -> Rectangle, Shape -> Circle**
    
3. **Multi-level:** One class inherits from parent then acts as parent for other.
    
    **Point -> Circle ->Cylinder**
    
4. **Multiple:** One class inherits from multiple parents. **Phone & Camera -> Smartphone**
    
5. Multi-path: A -> B,C. B & C -> D.** i.e. creating a path from A to D.

![[Screenshot from 2023-11-27 20-45-07.png]]
    ![[Screenshot from 2023-11-27 20-47-28.png]]
```cpp
class A {};
class B: virtual public A{}; 
//virtual use for this case.
class C: virtual public A{};
class D: public B,C{};
```