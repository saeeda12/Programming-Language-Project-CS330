#Functions, Parameters and Scope

###Amal Saeed


In this tutorial, we will learn how to write functions, how to pass parameters (or arguments) to them, and the scope and naming rules in C++.


####Declaring Functions
A **function** is a segment of code that performs a task, or tasks, and once written, can be called and used over and over again to perform that task. For example, you could write a function that calculates the area of a triangle, and then call that function whenever you want to calculate a triangle's area. Let's start with the first step of the function syntax: declaring a function! The function declaration, also known as a prototype, tells the compiler that a function exists. The general syntax is below:
```
return_type function_name(argument_list);
//OR
void function_name();
```
Above, `return_type` is the type of data that the function returns, and `argument_list` is the list of arguments - variable declarations - that the function requires, and is *not* required. If there is no return value, you type `void`. And always remember the semicolon! Let's explore with a simple multiplication function.
```
// Multiplication function
int mult(int a, int b);
```
Here, there is a return type - `int`, `mult` is the function name, and there are two arguments, separated by commas - `int a, int b`. And you finish the declaration with a semicolon! 

Now, from this function declaration, we need to define the function. The task we want `mult` to perform is multiplying together two integer numbers. The code block in which we will define `mult`'s task will be enclosed in braces {}. 
```
int mult(int a, int b) {
  code;
  return int;
}
```
We don't need a semicolon at the end of the function declaration because we are also defining it. Because our function returns a value of type `int`, it must have a return statement that returns a value of the same `return_type`, whereupon the functions terminates. Void functions can have a simple `return;` statement at the end of the function that does not return anything, but it is not required. In the code inside the function, it is best to put any variable declarations at the beginning of the code block - it is easiest to find that way.

The `mult` function's definition is below. It simply returns the product of `a` and `b`. 
```
// Function definition
int mult(int a, int b) {
  return a * b;
}
```

The third step is calling the function! When you call a function, you tell the computer to start executing another section of code - the code block in the function - before continuing with the rest of the program. The syntax is below:
```
function_name(data1, data2, ... , dataN);
//OR
function_name();
```
`data1`, etc. must be of the same type (or a type that can be easily converted. For example, if the argument type is `int`, then you can call the function and pass a `float` or `double` type value as the argument, and it would convert to an `int`. This is called a cast); it must also be in the same order as the arguments in the function definition. It must also have the same number of arguments as in the function definition. 

The `mult` function call is below:
```
// Function call
mult(5, 43);
```
This multiplies together 5 and 43.

A function must obviously be declared *or* defined before it can be called. If the function definition is at the end of the program, which is perfectly fine, and you call the function before it, you need to put its declaration at the beginning of the program so the computer knows that the function exists. Otherwise, the function definition can simply be placed at the beginning of the program, and that's that! A sample program is below:
```
// Multiplication program

#include <iostream>

// Function declaration
int mult(int a, int b);

int main(void) {
  using std::count;
  using std::cin;
  int num1, num2;  // Declare two integer variable in the same line
  cout << "Enter a number: ";
  cin >> num1;
  cout << "Enter another number: ";
  cin >> num2;
  cout << "\n The product of these two numbers is: " << mult(num1, num2) << ". \n";  // A \n means a newline
}

// Function definition
int mult(int a, int b) {
  return a * b;
}
```
You can place a function call inside a print statement, as seen in the last line of `main`.

p. 92
####Recursive Functions

