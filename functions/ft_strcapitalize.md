```c
char	*ft_strcapitalize(char *str)
{
	int	i;
	int	new;

	i = 0;
	new = 1;
	while (str[i] != '\0')
	{
		if ((str[i] | 32) - 'a' < 26 || (str[i] - '0' < 10))
		{
			if (new && (str[i] >= 'a' && str[i] <= 'z'))
			{
				str[i] = str[i] - 32;
			}
			else if (!new && (str[i] >= 'A' && str[i] <= 'Z'))
			{
				str[i] = str[i] + 32;
			}
			new = 0;
		}
		else 
			new = 1;
		i++;
	}
	return (str);
}
```
