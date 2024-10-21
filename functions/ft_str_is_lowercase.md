```c
int	ft_str_is_lowercase(char *str)
{
	if (*str == '\0')
	{
		return (1);
	}
	while (*str != '\0')
	{
		if (*str < 'a' || *str > 'z') // check if character is not between 'a' and 'z'
		{
			return (0); // if it is not retrun 0
		}
		str++; // increment to check next character
	}
	return (1); // skip if condition if character is between 'a' and 'z'
}
```
