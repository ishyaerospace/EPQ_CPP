# Memory Management in C++

Memory management is the process of controlling how much memory you program uses and how it is used. This includes creating, using and releasing memory when its no longer needed.

This would be important for Embedded systems

when creating a variable with a data type, C++ automatically handles the memory management by creating space in memory.

## Get Memory Size
you can get the memory size of variable using the sizeof operator
example: `sizeof(myInt)`

## does memory managemnet need to be used by developer?

for normal variables like integers, C++ takes care of this.
if developer wants to create memory manually while the program is running, for exaple: based on user input, then memory management can be done and cleaned up by developer

NOTE: If your program uses too much memory, or forgets to clean up memory it no longer needs, it can lead to slow performance or even crashes.

# C++ new and delete 

## new Keyword
lets developer manage memory theirself

`int* ptr = new int;`
`*ptr = 35;`
`cout << *ptr;`

this creates memory space for an integer using `new`, sores the value 35 in it and then prints using a pointer.

`new int` creates memory space for one integer
`ptr` stores the address of that space
`*ptr = 35;` stores the number 35
`cout << *ptr;` prints the value

## delete Keyword
when you create something with `new`, its your job to remove it when done.

this is done using the `delete` keyword

`delete ptr;` this tells C++ that your done with that memory and it can be cleaned up now. if you dont do this, a memory leak can occur, crashing your program over time.