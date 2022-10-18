# Studies-in-Memory-V
I was having trouble understanding pointers, so I made this as quick study in how declarations differ from pointer or integer.
I learned that a pointer holds an address to a variable, and if it does not have an address to a specified variable, it does holds its own address. A pointer take up memory dependent on the specified type evident in the declaration. Therefore an int* pointer holds an address for something specifically 4 bytes long as per the specified data type in declaration. 


#include<stdio.h>
int main()
{
    int* pointer;
    printf("Address of pointer: %p\n", &pointer);
}

Address of pointer: 0x7fffc4eab638
_____________

Thus, a pointer holds its own address.
We can also store the address of a declared int as such without specifying a alue for the declared int:

#include<stdio.h>
int main()
{
    int* pointer;
    int m;
    pointer = &m;
    printf("Address of pointer: %p\nAddress of m: %p\n", &pointer, &m);
}

Address of pointer: 0x7ffd3c75e2e8
Address of m: 0x7ffd3c75e2e4
_____________

What I learned is that everything requires memory because everything a computer does needs to have a set of commands to for its activity. Memory is best thought of as a big array. That array is taken up by a certain size of bytes depending on the data type.
I also learned that we use pointers to reuse values in separate functionsm and therefore eliminating a redeclaration of variables and their types whuch would only take up more memory over time.



