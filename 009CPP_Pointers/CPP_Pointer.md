# C++ Pointers
important for embedded systems
## Creating Pointers
A pointer is a variable that stores the memory address as its value.

a pointer variable points to a data type of the same tpe and is created with the "*" operator. The address of the variable you are working with is assigned to the pointer

example: 
`string food = "Pizza";`
`string* ptr = &food;`
A pointer variable, with the name ptr, that stores the address of food

# C++ Dereference
## get Memory address and value

`string food = "Pizza";  // Variable declaration`
`string* ptr = &food;    // Pointer declaration`

`// Reference: Output the memory address of food with the`
`pointer (0x6dfed4)`
`cout << ptr << "\n";`

`// Dereference: Output the value of food with the pointer (Pizza)`
`cout << *ptr << "\n";`

in this situation * is used in declaration creating a pointer variable, when not used in declaration, it acts as a dereference operator.

## modifying the pointer value
You can also change the pointer's value. But note that this will also change the value of the original variable:

