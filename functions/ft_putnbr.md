This function takes an integer and prints it digit by digit.

```c
void    ft_putnbr(int number) // the function takes an integer as a parameter
{
        char    digit; // 
        if (number >= 10) 
        {
                ft_putnbr(number / 10); 
        }
        digit = number % 10 + '0'; 
        write(1, &digit, 1);
}
```
