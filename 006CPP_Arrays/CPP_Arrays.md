# Arrays in C++

`string cars[4];`
comma seperated values assigned to the array:
`string cars[4] = {"Volvo", "BMW", "Ford", "Mazda"};`

## for each loop

`for (type variableName : arrayName) {`
`  // code block to be executed`
`}`

example code:

`int myNumbers[5] = {10, 20, 30, 40, 50};`

`for (int num : myNumbers) {`
`  cout << num << "\n";`
`}`

## get array size
sizeof(array) --> returns a size of a type in bytes
this i given by the ("number of items" x "type size")
type size is how much bytes is taken up from the data type

to get the size of an array you will need to divide the size of the array by the size of the first element in the array.

