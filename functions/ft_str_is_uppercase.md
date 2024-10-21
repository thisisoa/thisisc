```c
int	ft_str_is_uppercase(char *str)
{
	if (*str == '\0')
	{
		return (1);
	}
	while (*str != '\0')
	{
		if (*str < 'A' || *str > 'Z') // check if the character is not between 'A' and 'Z'
		{
			return (0); // if it is true return 0
		}
		str++; // increment to check next character
	}
	return (1); // return 1 if the character is between 'A' and 'Z'
}
```
