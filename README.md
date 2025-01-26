Your code is almost correct but has a logical issue in the `printString` function. The loop in `printString` does not terminate, leading to an infinite loop because there is no condition to stop when the string ends. In C, strings are terminated with a null character (`'\0'`), and the loop should check for this to stop iterating.

Here’s the corrected version of your code:

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

### Key Fixes:
1. **Proper Loop Termination in `printString`:**
   - The `for` loop now checks for the null character (`'\0'`) to stop.
   
2. **Added a Function Call in `main`:**
   - `printString(firstname)` is called to print the string.

3. **Optional Formatting:**
   - Added a newline (`\n`) after printing the string for better output formatting.

### Output:
```
saujanya
``` 

Now your code will correctly print the string `"saujanya"`.# String
