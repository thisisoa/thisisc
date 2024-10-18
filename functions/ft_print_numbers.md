The function that displays all digits, on a single line, by ascending order.

```c
#include <unistd.h>

void ft_print_numbers(void) // void means taking no parameters and returning nothing
{
    char digit = '0'; //initialize char variable name digit and assign an initial value as zero
    
    while (digit <= '9') // conditional loop -> until digit less than or equal to nine
    {
        write(1, &digit, 1); // display the digit
        digit++; // increment digit to move to the next character.
    }
    write(1, "\n", 1); // add a newline
}

int main()
{
    ft_print_numbers();
    return 0;
}
```

Here's the output:

```c
0123456789
```
