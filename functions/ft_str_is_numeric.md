```c
int	ft_str_is_numeric(char *str)
{
	if (*str == '\0')
	{
		return (1);
	}
	while (*str != '\0')
	{
		if (*str < '0' || *str > '9') // character is smaller than '0' or bigger than '9'
		{
			return (0); // if it is true, retrun 0
		}
		str++; increment to move the next character
	}
	return (1); // skip if condition if character is between 0 and 9
}
```
