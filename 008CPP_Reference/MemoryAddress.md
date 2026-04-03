# Memeory address in C++

"&" operator can be used to create reference variables however it can also be used to get the memeory address of a variable.

To access it, we use the "&" operator to return where the variable is stored.

`string food = "Pizza";`
`cout << &food; // Outputs 0x6dfed4` <-- hex form

this is useful as it allows for references and pointers that are importnatn in C++ as they give the ability to manipulate the data in a computer's memory - which can reduce the code and improve the performance