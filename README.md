
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

Here’s an example of how the corrected program would behave when executed:

### **Input (User enters in stdin)**
```
Hello, World!
```

### **Output**
```
Hello, World!

Hello, World!
```

### **Explanation**
1. `fgets(str, 100, stdin);` reads `"Hello, World!\n"` (including the newline `\n`).
2. `puts(str);` prints it, adding an extra newline.
3. `printString(str);` prints the string character by character, keeping the newline.

If you don't want the extra newline from `puts`, you can modify `fgets` to remove it:

#### **Updated Code (Remove Newline from `fgets`)**
```c
#include <stdio.h>

void printString(char arr[]) {
    for (int i = 0; arr[i] != '\0'; i++) {
        printf("%c", arr[i]);
    }
    printf("\n");
}

int main() {
    char str[100];
    fgets(str, 100, stdin);

    // Remove newline if present
    int i = 0;
    while (str[i] != '\0') {
        if (str[i] == '\n') {
            str[i] = '\0';  // Replace newline with null character
            break;
        }
        i++;
    }

    puts(str);
    printString(str);

    return 0;
}
```

### **Output for Same Input**
```
Hello, World!
Hello, World!
```

Now, there’s no extra newline between outputs. Let me know if you need further changes!



Here’s how the corrected program runs with an example input and output:  

### **Fixed Code:**  
```c
#include <stdio.h>

void printString(char arr[]); 
int countLength(char arr[]);

int main() {
    char name[100];
    
    printf("Enter a string: ");
    fgets(name, 100, stdin);

    printf("Length is: %d\n", countLength(name));
    printf("You entered: ");
    printString(name);

    return 0;
}

int countLength(char arr[]) {
    int count = 0;
    while (arr[count] != '\0') {
        count++;
    }

    // Remove trailing newline character (if present)
    if (count > 0 && arr[count - 1] == '\n') {
        return count - 1;
    }

    return count;
}

void printString(char arr[]) {
    for (int i = 0; arr[i] != '\0'; i++) {
        printf("%c", arr[i]);
    }
}
```

---

### **Example Execution:**  
#### **Input:**  
```
Enter a string: Hello World
```

#### **Output:**  
```
Length is: 11
You entered: Hello World
```

---

### **Explanation:**
1. **User enters** `"Hello World"` (11 characters + `\n` from `fgets`).
2. **`countLength` function:**  
   - Counts the characters in the array.
   - Detects the newline character (`\n`) and excludes it.
   - Returns `11` instead of `12` (correct length).
3. **`printString` function:**  
   - Prints the string properly without adding an extra newline.  

Let me know if you need modifications!
