
### Corrected Code:
```c
#include <stdio.h>

void printString(char arr[]);

int main() {
    char firstname[] = "saujanya";
    
    printString(firstname); // Call the function to print the string
    
    return 0;
}

void printString(char arr[]) {
    for (int i = 0; arr[i] != '\0'; i++) { // Check for the null terminator
        printf("%c", arr[i]);
    }
    printf("\n"); // Optional: Add a newline for better formatting
}
```

#
### Output:
```
saujanya
``` 

Now your code will correctly print the string `"saujanya"`.# String

```
#include <stdio.h>

void printString(char arr[]);

int main() {
    char name[50];
    scanf("%49s", name); // Limit input size
    printf("Your name is %s\n", name);
    printString(name); // Call the function
    return 0;
}

void printString(char arr[]) {
    for (int i = 0; arr[i] != '\0'; i++) {
        printf("%c", arr[i]);
    }
    printf("\n"); // Print newline for better output formatting
}

```
Let's analyze the expected output of the corrected code.

### **Input:**
```
Alice
```

### **Output:**
```
Your name is Alice
Alice
```

### **Explanation:**
1. The program reads the input `"Alice"`.
2. It prints `"Your name is Alice"`.
3. The `printString(name)` function is called, which prints each character of `"Alice"` sequentially.
4. A newline (`\n`) is added at the end for better formatting.

Would you like me to run this code for verification?
