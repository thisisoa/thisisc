The  strncpy()  function is similar, except that at most n bytes of src are copied.  

*Warning*: If there is no null byte among the first n bytes of src, the string placed in dest will not be null-terminated. If  the  length of src is less than n, strncpy() writes additional null bytes to dest to ensure that a total of n bytes are written.

```c
char    *ft_strncpy(char *dest, char *src, unsigned int n)
/*
We have 3 parameters,
dest for destination,
src for source,
n for max number of characters to copy
*/
{       
        int     i; // create a counter
        i = 0;

        while (i < n && src[i] != '\0') //
        {
                dest[i] = src[i];
                i++;
        }

        while (i < n)
        {
                dest[i] = '\0';
                i++;
        }       
        return (dest); 
}
```

### What is unsigned keyword?
Unsigned defines hold zero (0) and non-negative (positive) values.

