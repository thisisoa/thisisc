This is a function that displays the character passed as a parameter.

```c
#include <unistd.h>

void	ft_putchar(char c) // function takes single char parameter named c
{
	write(1, &c, 1); // write function takes 3 arguments
/*
The first argument 1 represents the file descriptor for standard output (stdout).
The second argument &c is the address of the character to be written.
The third argument 1 specifies that we want to write 1 byte (the size of a char).
*/
}

int main(void)
{
	ft_putchar('A');
}
```

Here's the output:
```c
A
```
