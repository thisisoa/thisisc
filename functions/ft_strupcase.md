This function that transforms every letter to uppercase.

The header file for the output

```c
#include <stdio.h>
```
```c
char	*ft_strupcase(char *str)
{
	char	*temp;
	temp = str;
	
	while (*temp != '\0')
	{
		if (*temp >= 'a' && *temp <= 'z')
		{
			*temp = *temp - 32;
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
	char	str[] = "This is a test";
	ft_strupcase(str);
	printf("%s\n", str);	
	return 0;
}
```
