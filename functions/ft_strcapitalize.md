This function that capitalizes the first letter of each word (It is a string of alphanumeric characters) and transforms all other letters to lowercase.

```c
char	*ft_strcapitalize(char *str)
{
	int	i; // create a counter
	int	new; // create flag to understand if it is a new word

	i = 0;
	new = 1;
	while (str[i] != '\0') //check if the array is empty or not
	{
/* Check if alphanumeric characters
(str[i] >= 'a' && str[i] <= 'z') ||
(str[i] >= 'A' && str[i] <= 'Z') ||
(str[i] >= '0' && str[i] <= '9')
*/
		if ((str[i] | 32) - 'a' < 26 || (str[i] - '0' < 10)) // Check if characters are alphanumeric characters
		{
			if (new && (str[i] >= 'a' && str[i] <= 'z')) // if it is a new start and character is lowercase 
			{
				str[i] = str[i] - 32; // convert case to Upper
			}
			else if (!new && (str[i] >= 'A' && str[i] <= 'Z')) // if it is not a new start and character is uppercase
			{
				str[i] = str[i] + 32; // convert case to Lower
			}
			new = 0; // set flag to zero
		}
		else 
			new = 1; // set flag to 1 to approve it is a new start
		i++; // increment to check next caharcter
	}
	return (str);
}
```
