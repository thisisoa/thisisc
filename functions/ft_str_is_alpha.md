```c
#include <stdio.h>

int	ft_str_is_alpha(char *str)
{
        if(*str == '\0')
        {
                return (1);
        }
	while(*str != '\0')
	{
		if((*str < 'a' || *str > 'z') && (*str < 'A' || *str > 'Z'))  // check if characters are not alphabetical characters
		{	
			return (0); // if it is true, return 0
		}
		str++;	//increment the str to move the next character
	}
	return (1); // skip if and return if chracter is alphabetical
}

int main()
{
	char 	*str;
       	str = "";
	printf("Check Empty: %i\n", ft_str_is_alpha(str));
	str = "42";
	printf("Check Other Chars: %i\n", ft_str_is_alpha(str));
	str = "Heyoooo";
        printf("Check Only Alpha: %i\n", ft_str_is_alpha(str));

	return 0;
}
```
