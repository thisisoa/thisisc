This function displays the alphabet in lowercase, on a single line, by ascending order, starting from the letter ’a’.

```c
#include <unistd.h>

void	ft_print_alphabet(void)
{
	char letter; // create a character variable with the name letter

	letter = 'a'; // initialize letter with 'a'
	while (letter <= 'z') // conditional loop -> until letter equals or less than 'z'
	{
		write(1, &letter, 1); // display the current letter
		letter++; // increment letter to move to the next character
	}
}

int main()
{
	ft_print_alphabet(); // call ft_print_alphabet function
	return 0;
}
```

The output is
```c
abcdefghijklmnopqrstuvwxyz
```
