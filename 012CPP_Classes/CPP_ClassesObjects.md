# classes/objects in C++

`class MyClass {       // The class`
`  public:             // Access specifier`
`    int myNum;        // Attribute (int variable)`
`    string myString;  // Attribute (string variable)`
`    void myMethod(){`
`         //code`
`    }`
`};`

in main function:
`MyClass class;` this creates the object
`class.myMethod();` calls method of object

using what was learnt about the syntax of name spaceses we can use a technique to define methods outside of the class.
`class MyClass{`
`    public:`
`    void myMethod // declared method`
`}`

`//Method/function defined outside the class`
`void MyClass::myMethod() {`
`  cout << "Hello World!";`
`}`

:: is the scope resolution operator


## constructors
constructor is a special method that automatically called when an object is created

to do this you need to have a method with the same name as the class name with parenthesis "()"

`class MyClass {     // The class`
`  public:           // Access specifier`
`    MyClass(int x) { code }    // Constructor`
`};`

in main function:
`MyClass class(10);` x is now 10 in the class.

this can also be done by defining outside of class like a regular method.

## constructor overloading
have more than one constructor in the same class, must have different number of parameters 
* used for flexibility when creating objects
* to set defualt or custom values
* to reduce repetitive code

`class Car {`
`  public:`
`    string brand;`
`    string model;`

`    Car() {`
`      brand = "Unknown";`
`      model = "Unknown";`
`    }`

`    Car(string b, string m) {`
`      brand = b;`
`      model = m;`
`    }`
`};`


## access specifiers
public keyword is the access specifier. 
public means it can be accessed and modified outside of class.

there are three access specifiers
* public - members are accessible from outside of class
* private - members cannot be accessed or read from outside of class
* protected - members cannot be accessed from outside of class unless it is an inherited class

## encapsulation
is to hide sensitive information from users
this is done by declaring attributes and methods as private.

to access these attributes, you need get and set methods.

`private:`
`    int x;`
`public:`
`    void setx(int input){`
`        x = input;`
`    }`
`    void getx(){`
`        return x;`
`    }`


## friend functions
normally get and set methods are used to access private attributes using public methods

you can use special functions called friend functions to access them directly.
a friend function is not a memeber of the class. but it is allowed to access the classe's private data:

example:
`class Employee {`
`  private:`
`    int salary;`

`  public:`
`    Employee(int s) {`
`      salary = s;`
`    }`

`    // Declare friend function`
`    friend void displaySalary(Employee emp);`
`};`

`void displaySalary(Employee emp) {`
`  cout << "Salary: " << emp.salary;` // defined
`}`

## inheritance
inheritance allows one class to reuse attrbiutes and methods from another.

* derived class (child) - class that inherits from another
* base class (parent) - class being inherited from

to inherit from a class use the : symbol

// Derived class
`class Car: public Vehicle {code}`
Car is child
Vehicle is parent