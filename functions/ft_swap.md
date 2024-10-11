```c
#include <unistd.h>

void	ft_swap (int *a, int *b)
{
	int temp;
	temp = *a;
	*a = *b;
	*b = temp;
}

int main ()
{
	int x = 5;
	int y = 8;
	ft_swap (&x, &y);
	write (1, "x", 2);
	return (0);
}
```
