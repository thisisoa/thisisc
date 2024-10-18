This function writes a string of characters to the standard output (STDOUT)

```c
#include <unistd.h>

void	ft_putstr(char *str) // this function takes character pointer array as a parameter
{
	while (*str != '\0') // conditional loop -> continue until end of the sring. '\0' null terminator is the end.
	{
		write (1, str, 1); // 1 (standart ouput), str (address of the character), 1 (size, here only 1 byte)
		str++; // increment str for the next character.
	}
}
```
Here is an example usage of this function:

```c
#include <unistd.h>

void ft_putstr(char *str);

int main()
{
    char *message = "Hello, World!";
    ft_putstr(message);
    write(1, "\n", 1);  // add a new line
    return 0;
}
```

Here is the output:
```c
Hello, World!
```
