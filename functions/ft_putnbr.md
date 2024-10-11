```c
void    ft_putnbr(int number)
{
        char    digit; 
        if (number >= 10) 
        {
                ft_putnbr(number / 10); 
        }
        digit = number % 10 + '0'; 
        write(1, &digit, 1);
}
```
