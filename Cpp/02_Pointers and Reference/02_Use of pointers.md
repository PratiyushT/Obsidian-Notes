

#### Use of pointer
For example, we have created a [[03_Stack, Heap and Pointers|value in heap]]. To access the value we create a pointer in stack and point towards the memory location of the value at heap. Hence, program can now access the heap. This also involves file access. Files are not in the stack or code section of the memory. Hence, we need to use pointers to access them. ==**Anything**== that is not in code section or stack requires pointer to access them. This is why we can do system programming, device drivers or OS using C++.




