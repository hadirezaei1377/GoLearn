Go is a cross-platform, open source programming language
Go can be used to create high-performance applications
Go is a fast, statically typed, compiled language that feels like a dynamically typed, interpreted language

What is Go Used For?
Web development (server-side)
Developing network-based programs
Developing cross-platform enterprise applications
Cloud-native development

Why Use Go?
Go is fun and easy to learn
Go has fast run time and compilation time
Go supports concurrency
Go has memory management
Go works on different platforms (Windows, Mac, Linux, Raspberry Pi, etc.)

Compilation time refers to translating the code into an executable program
Concurrency is performing multiple things out-of-order, or at the same time, without affecting the final outcome
Statically typed means that the variable types are known at compile time

A Go file consists of the following parts:

Package declaration
Import packages
Functions
Statements and expressions

fmt.Println("Hello World!") is a statement.
In Go, statements are separated by ending a line (hitting the Enter key) or by a semicolon ";".
Hitting the Enter key adds ";" to the end of the line implicitly (does not show up in the source code).

Go Variable Types
In Go, there are different types of variables, for example:

int- stores integers (whole numbers), such as 123 or -123
float32- stores floating point numbers, with decimals, such as 19.99 or -19.99
string - stores text, such as "Hello World". String values are surrounded by double quotes
bool- stores values with two states: true or false

Declaring (Creating) Variables
In Go, there are two ways to declare a variable:

1. With the var keyword:
Use the var keyword, followed by variable name and type:

Syntax
var variablename type = value
Note: You always have to specify either type or value (or both).

2. With the := sign:
Use the := sign, followed by the variable value:

Syntax
variablename := value
Note: In this case, the type of the variable is inferred from the value (means that the compiler decides the type of the variable, based on the value).

Note: It is not possible to declare a variable using :=, without assigning a value to it.

Variable Declaration With Initial Value
If the value of a variable is known from the start, you can declare the variable and assign a value to it on one line:
In Go, all variables are initialized. So, if you declare a variable without an initial value, its value will be set to the default value of its type:

func main() {
  var a string
  var b int
  var c bool

  fmt.Println(a)
  fmt.Println(b)
  fmt.Println(c)
}

Go variable naming rules:

A variable name must start with a letter or an underscore character (_)
A variable name cannot start with a digit
A variable name can only contain alpha-numeric characters and underscores (a-z, A-Z, 0-9, and _ )
Variable names are case-sensitive (age, Age and AGE are three different variables)
There is no limit on the length of the variable name
A variable name cannot contain spaces
The variable name cannot be any Go keywords
Multi-Word Variable Names
Variable names with more than one word can be difficult to read.

There are several techniques you can use to make them more readable:

Camel Case
Each word, except the first, starts with a capital letter:

myVariableName = "John"
Pascal Case
Each word starts with a capital letter:

MyVariableName = "John"
Snake Case
Each word is separated by an underscore character:

my_variable_name = "John"

Go Constants
If a variable should have a fixed value that cannot be changed, you can use the const keyword.

The const keyword declares the variable as "constant", which means that it is unchangeable and read-only.

const CONSTNAME type = value
Note: The value of a constant must be assigned when you declare it.

Constant names follow the same naming rules as variables
Constant names are usually written in uppercase letters (for easy identification and differentiation from variables)
Constants can be declared both inside and outside of a function
Constant Types
There are two types of constants:

Typed Constants
Typed constants are declared with a defined type:

Example
const A int = 1

func main() {
  fmt.Println(A)
}
Untyped Constants
Untyped constants are declared without a type:

const A = 1

func main() {
  fmt.Println(A)
}

Constants: Unchangeable and Read-only
When a constant is declared, it is not possible to change the value later:

Example

func main() {
  const A = 1
  A = 2
  fmt.Println(A)
}
Result:

./prog.go:8:7: cannot assign to A

Go has three functions to output text:

Print()
Println()
Printf()

The Print() function prints its arguments with their default format.

Example
Print the values of i and j:


func main() {
  var i,j string = "Hello","World"

  fmt.Print(i)
  fmt.Print(j)
}
Result:

HelloWorld
Tip: \n creates new lines.

If we want to add a space between string arguments, we need to use " ":

func main() {
  var i,j string = "Hello","World"

  fmt.Print(i, " ", j)
}
Result:

Hello World

The Println() function is similar to Print() with the difference that a whitespace is added between the arguments, and a newline is added at the end:

func main() {
  var i,j string = "Hello","World"

  fmt.Println(i,j)
}
Result:

Hello World

The Printf() function first formats its argument based on the given formatting verb and then prints them.
Here we will use two formatting verbs:

%v is used to print the value of the arguments
%T is used to print the type of the arguments

func main() {
  var i string = "Hello"
  var j int = 15

  fmt.Printf("i has value: %v and type: %T\n", i, i)
  fmt.Printf("j has value: %v and type: %T", j, j)
}
Result:

i has value: Hello and type: string
j has value: 15 and type: int

Formatting Verbs for Printf()

Verb	Description
%v	Prints the value in the default format
%#v	Prints the value in Go-syntax format
%T	Prints the type of the value
%%	Prints the % sign

Go Data Types
Data type is an important concept in programming. Data type specifies the size and type of variable values.

Go is statically typed, meaning that once a variable type is defined, it can only store data of that type.

