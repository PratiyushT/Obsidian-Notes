
#### Functions in cstring:

1. `strlen(string); //Show len of string`
    
2. `strcat(dest, source); //Concatenate dest + source and store in dest`
    
3. `strncat(dest, soruce, length_of_source); //Same as above but specify len of source`
    
4. `strcpy(destination, source, length_of_source); //Copy source to dest`
---
#### Functions in cstring pt.2 (substrings):

1. `strstr(main, substring); //Find appearance of substring from main and return portion of main after that occurence.`
    
2. `strchar(main, char); //Same as above but will take char and not a substring.`
    
3. `strrchar(main, char); //Same as above but will check from right to left of main.`
    
4. `strcmp(str1, str2); // Checks if str1 come before or after str2 in dictionary order returns diff between their ASCII code`.
---
#### Functions in cstring pt.3 (Int conversion and tokenization):

1. `strtof(string, end, base) //String to float`
    
2. `strtol(string, end, base) //String to long.`
    
    Note: `NULL` is generally the end. Base refers to number system. E.g. 10 for decimal.
    
3. `strtok(string, symbols) //Understand from example.`
    
    ```cpp
     char s1[20] = "x=10; y=20; z=30";
    2.     char *token = strtok(s1, "=; ");
    3.     while(token !=NULL){
    4.         cout << token << endl;
    5.         token = strtok(nullptr, "=; ");
    6.     }
    7. Output: 
    
// x
// 10
// y
// 20
//. z
//30
```
    **Basically print stuff other than the specified symbols by creating a loop. Called as tokenization.**
---