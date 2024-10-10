# Pointers in C

Here are some good stuff to understand pointers!

### Intro
Think that invite you a party at my house by just showing the photo of the house!
Insane right! and you asked me about the address! Yes only if I give you the exact address, this make it much more easier to find that party house! So enjoy!

Copy the below code to your IDE/VIM:

```c

#include <stdio.h>
int main()
{
        int     alpha;

        alpha = 27;
        printf("Integer variable 'alpha' has a value: %i\n", alpha);
        printf("Integer variable 'alpha' memory occupation: %lu\n", sizeof(alpha));
        printf("Integer variable 'alpha' has an address: %p\n", &alpha);

        return 0;
}
```
So as you see;
- every variable can get a value (use **%i** or **%d** placeholders for integers)
- every variable occupies the memory (use **%lu** placeholder and **sizeof()** to see)
- every variable has an address (use **%p** placeholder and referencing operator **&** to see)

When you run this main function, the result should look similar to this:
```
Integer variable 'alpha' has a value: 27
Integer variable 'alpha' memory occupation: 4
Integer variable 'alpha' has an address: 0x7ffea8115f44
```
### Now we can say that pointer is a variable that holds a memory location!
- A pointer holds the address of a variable or buffer in the code
- A pointer represents a memory location
- A pointer has a prefix, * asterisk, which represents the data stored in the memory location
- A pointer can be modified
- The pointer can change or manipulate data at its address that the pointer holds.

### Declaring and Using Pointers
- It has a data type like int, char 
- It has a variable name prefixed by an asterisk *ptr
- It need to be initialized before it is used
- **THIS IS IMPORTANT!** It is assigned the address of another variable, one of the same data type. 
For int, it is int. For char it is char!
- The ampersand operator **&** fetches a variables' address.
- It can be assigned any kind of memory; allocated chunk or buffer 

### Let's Test What We've Just Learned

Copy the below code to your IDE/VIM:
**The Address**

```c

#include <stdio.h>

int main()
{
        int var; // declared an integer variable
        int *ptr; // declared an integer pointer variable

        var = 55; // integer variable var got a value
        ptr = &var; // pointer ptr's address got matched with integer variable var's address
        // always use & to mean variables' address

        printf("The address of integer 'var' variable: %p\n", &var); // use & to fetch variables' address
        printf("The address of pointer 'ptr' variable: %p\n", ptr); // use %p placeholder to print address

        return 0;
}
```
When you run this main function, the result should look similar to this:
```
The address of integer 'var' variable: 0x7ffd9a0c631c
The address of pointer 'ptr' variable: 0x7ffd9a0c631c
```
As you see they are showing exactly the same address! Good job!
Let's get more results by adding more lines of code and print out.

Copy the below code to your IDE/VIM:
**The Value**

```c

#include <stdio.h>

int main()
{
        int var; 
        int *ptr;

        var = 55; 
        ptr = &var;

        printf("The value of integer 'var' variable: %d\n", var); //use %d or %i to get the value
        printf("The pointer 'ptr' has an address %p and a value %i\n", ptr, *ptr); // use %p to get address 
        // we use ptr for address output and use *ptr with * asterisk for the value output

        return 0;
}
```
When you run this main function, the result should look similar to this:
```
The value of integer 'var' variable: 55
The pointer 'ptr' has an address 0x7fffc63d546c and a value 55
```
As you see the values are matched.
Since their addresses are same, actually they are :100: same.
Let's see how they are deeply connected by adding more lines of code and print out.

Copy the below code to your IDE/VIM:
**The Manipulation (Changing the Value)**

```c

#include <stdio.h>

int main()
{
        int var; 
        int *ptr;

        var = 55; 
        ptr = &var;

        *ptr = 42; // the pointer assigned a new value to the memory location
        printf("The value of integer 'var' variable: %d\n", var); // integer variable 'var' now represents the new value

        return 0;
}
```
When you run this main function, the result should look similar to this:
```
The value of integer 'var' variable: 42
```

As you see the pointer manipulated the integer variable and changed its value.
These are all happened, because they are located at the same address and that address has only one value.
One more time! Good job finding the party house. Since you arrived let's start the party!
