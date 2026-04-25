# Division-program-using-goto-for-error-handling
Write a C program that performs division of two user inputs and uses goto  to handle errors like division by zero or invalid input by redirecting control for re-entry.

Proram:

```
#include <stdio.h>

int main() {
    float num1, num2, result;

start:
    printf("Enter two numbers: ");
    
    if(scanf("%f %f", &num1, &num2) != 2) {
        printf("Invalid input! Try again.\n");
        while(getchar() != '\n'); // clear buffer
        goto start;
    }

    if(num2 == 0) {
        printf("Division by zero is not allowed! Try again.\n");
        goto start;
    }

    result = num1 / num2;
    printf("Result = %.2f\n", result);

    return 0;
}
```

Output:

<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/a5d47c9f-3055-4792-8a36-4198e25af14b" />
