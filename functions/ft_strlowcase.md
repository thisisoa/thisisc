This function that transforms every letter to lowercase.

The header file for the output
```c
#include <stdio.h>
```
The function:
```c
char	*ft_strlowcase(char *str)
{
	char	*temp;

	temp = str;
	while (*temp != '\0')
	{
		if (*temp >= 'A' && *temp <= 'Z')
		{
			*temp = *temp + 32;	
		}
		temp++;
	}
	return (str);
}
```
Main function for the output:
```c
int main()
{
	char str[] = "HARFLERI KUCULT ama bunlar kalsin";
	ft_strlowcase(str);
	printf("%s\n", str);
	return 0;
}
```
