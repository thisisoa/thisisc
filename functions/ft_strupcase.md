This function that transforms every letter to uppercase.

The header file for the output

```c
#include <stdio.h>
```
```c
char	*ft_strupcase(char *str)
{
	char	*temp; // create a temporary pointer array
	temp = str; // assign values to temp to keep the original string
	
	while (*temp != '\0') // check if temp array is empty and if it is not move to next command 
	{
		if (*temp >= 'a' && *temp <= 'z') // check if the character is between 'a' and 'z'
		{
			*temp = *temp - 32; // if it is true, conver the case to Uppercase
		}	
		temp++; // increment to check the next character
	}
	
	return (str); // when temp array comes to end return to result
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
