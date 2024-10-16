This function is a copy of strcpy function.
The  strcpy() function copies the string pointed to by src, including the terminating null byte ('\0'), to the buffer pointed to by dest.

The strings may not overlap, and the destination string dest must be large enough to receive the copy.

```c
char *ft_strcpy(char *dest, char *src) //src for source, dest for destination
{
        int     i; //create a counter
        i = 0;

        while (src[i] != '\0') //conditional loop -> run until source hits the end
        {
                dest[i] = src[i]; //copying -> match characters in array at each step
                i++; //increase counter for next character
        }
        dest[i] = '\0'; //the counter reached the last, close the string.
        return dest; //finalize the function
}
```
If you check man strcpy in the Terminal. You will see BUGS sections.
BUGS:
If  the  destination  string of a strcpy() is not large enough, then anything might happen. Overflowing fixed-length string buffers is a favorite cracker technique for taking complete control of the machine. Anytime a program reads or copies data into  a  buffer, the program first needs to check that there's enough space.This may be unnecessary if you can show that overflow is impossible, but be careful:  programs  can  get changed over time, in ways that may make the impossible possible.

Let's take this warning into count! and add a control function runs.
```c
#include <string.h>
#include <stdio.h>

char *ft_strcpy(char *dest, char *src) //src for source, dest for destination
{
        int     i; //create counter
        i = 0;

        if (strlen(src) >= sizeof(dest)) // check if the length of source smaller or at least eqaul to destination.
        {
                printf("Buffer Error\n"); //if it is not, show message
                return NULL; //finalize function as returning empty
        }

        while (src[i] != '\0') //conditional loop -> run until source hits the end
        {
                dest[i] = src[i]; //copying -> match characters in array at each step
                i++; //increase counter for next character
        }
        dest[i] = '\0'; //the counter reached the last, close the string.
        return dest; //finalize the function by returning destination
}
```
