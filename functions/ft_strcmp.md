This function compares the two strings s1 and s2.  The locale is not taken into account (for a locale-aware comparison, see strcoll(3)).  The  comparison is done using unsigned characters.

- 0, if the s1 and s2 are equal;
- a negative value if s1 is less than s2;
- a positive value if s1 is greater than s2.

```c
int	ft_strcmp(char *s1, char *s2)
{
	while (*s1 && (*s1 == *s2))
	{
		s1++;
		s2++;
	}

	return *(unsigned char *)s1 - *(unsigned char *)s2; 
}
```
Let's add the heder file for printf function

```c
#include <stdio.h>
```

Let's test the result:

```c
int main()
{
	char *s1 = "42";
	char *s2 = "42";
	char *s3 = "FortyTwo";

	printf("S1 and S2: %i\n", ft_strcmp(s1, s2));
	printf("S2 and S3: %i\n", ft_strcmp(s2, s3));
	printf("S3 and S1: %i\n", ft_strcmp(s3, s1));		
	return 0;
}
```

Here's the result:
```c
S1 and S2: 0
S2 and S3: -18
S3 and S1: 18
```
```
