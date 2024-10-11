```c
#include <stdio.h>

int ft_strlen(char *str)
{
    int count = 0;
    while (*str != '\0')
    {
        count++;
        str++;
    }
    return count;
}

int main()
{
    char *test_string = "Hello, world!";
    int length = ft_strlen(test_string);
    printf("The length of '%s' is %d\n", test_string, length);
    return 0;
}
```
