# C++ Syntax

code:
`#include <iostream>`
`using namespace std;`

`int main() {`
`  cout << "Hello World!";`
`  return 0;`
`}`

`#include <iostream>` is a header file library, lets us work with input and output objects such as cout. headers add functionaity to C++ programs

`using namspace std` means that we can use names for objects and variables from the standard library

`int main()` function that runs the main code within the {}.

`return 0;` ends the main function

## omitting Namespace

code without namespace:
`#include <iostream>`

`int main() {`
`  std::cout << "Hello World!";`
`  return 0;`
`}`

`std::` makes it clear where names come from and avoids name conflicts in larger programs


## user input

`cin >> x;`