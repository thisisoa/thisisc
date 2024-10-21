```c
int	ft_str_is_printable(char *str)
{
	if (*str == '\0')
	{
		return (1);
	}
	while (*str != '\0')
	{
		if (*str < 32 || *str > 126) // check if the character is smaller than 32 and bigger than 126 in ASCII table
		// simply find non-printable ones - 32 is SPACE printable, 127 is DEL which is not printable  
		{
			return (0); // if it is not printable return 0
		}
		str++; // increment to check next character
	}
	return (1); // skip if condition and return 1 if the character is printable
}
```
