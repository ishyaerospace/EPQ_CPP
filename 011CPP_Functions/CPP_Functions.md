# Functions
already done functions for python and JavaScript. So I already know the syntax. therefore I will skip some content and get to the new content.

## pass by reference

`void changeValue(int &num) {`
`  num = 50;`
`}`

`int main() {`
`  int value = 10;`
`  changeValue(value);  // Call the function and change the ``value to 50`
`  cout << value; `
`  return 0;`
`}`

the "&" symbol is used to pass a reference. this allows the function to change the value of the original variable and not the local variable within the scope(function scope).

## passing struct by value

struct Car { // the struct
};

void myFunction(Car c) { // function that has the struct passed through. to access values from the struct use: c.{variable}
}

int main() {
  Car myCar = {content}; // initialise and fill content
  myFunction(myCar);
  return 0;
}


Note: Since the structure is passed by value, the function gets a copy of the structure.

This means that the original data is not changed.

## passing struct by reference

same syntax but using "&" in functions arguament.

myFunction(Car &c)

## Function overloading
Function overloading allows multiple functions to have the same name, as long as their parameters are different in type or number. this has been seen in the python course that was done.

for example: 
int myFunction(int x)
float myFunction(float x)
double myFunction(double x, double y)

this is useful as you dont have make multiple functions that do the same thing but have different names

for example:
`int plusFunc(int x, int y) {`
`  return x + y;`
`}`

`double plusFunc(double x, double y) {`
`  return x + y;`
`}`

`int main() {`
`  int myNum1 = plusFunc(8, 5);`
`  double myNum2 = plusFunc(4.3, 6.26);`

`  cout << "Int: " << myNum1 << "\n";`
`  cout << "Double: " << myNum2;`
`  return 0;`
`}`

this works with functions that have different number of parameters

## C++ Recursion
recursing is a technique of making a function call itself. provides a way to break complicated problems into simple problems. 

Example:

`int sum(int k) {`
`  if (k > 0) {`
`    return k + sum(k - 1);`
`  } else {`
`    return 0;`
`  }`
`}`

what this does is it calls sum() it adds parameter k to the sum of all numbers smaller than k and returns the result.

NOTE: developers should be careful with recursion as it can be quite easy to slip into wiring a function which never termincates or uses excess memory/cpu power.


## C++ Lambda Functions
lambda function is a small, anonymous function. it can be written directly in the code, it is useful when a function is needed quickly without naming or declaring one seperately.

Syntax:
`[capture] (parameters) { code };`

capture clause []
you can use [] brackets to give a lambda access to variables outside of it.
example:
`int main() {`
`  int x = 10;`
`  auto show = [x]() {`
`    cout << x;`
`  };`
