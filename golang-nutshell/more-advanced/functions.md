A function is a block of statements that can be used repeatedly in a program.

A function will not execute automatically when a page loads.

A function will be executed by a call to the function.

Create a Function
To create (often referred to as declare) a function, do the following:

Use the func keyword.
Specify a name for the function, followed by parentheses ().
Finally, add code that defines what the function should do, inside curly braces {}.
Syntax
func FunctionName() {
  // code to be executed
}
Call a Function
Functions are not executed immediately. They are "saved for later use", and will be executed when they are called.

In the example below, we create a function named "myMessage()". The opening curly brace ( { ) indicates the beginning of the function code, and the closing curly brace ( } ) indicates the end of the function. The function outputs "I just got executed!"


Parameters and Arguments
Information can be passed to functions as a parameter. Parameters act as variables inside the function.

Parameters and their types are specified after the function name, inside the parentheses. You can add as many parameters as you want, just separate them with a comma:

Syntax
func FunctionName(param1 type, param2 type, param3 type) {
  // code to be executed
}
Function With Parameter Example
The following example has a function with one parameter (fname) of type string. When the familyName() function is called, we also pass along a name (e.g. Liam), and the name is used inside the function, which outputs several different first names, but an equal last name:

Example
package main
import ("fmt")

func familyName(fname string) {
  fmt.Println("Hello", fname, "Refsnes")
}

func main() {
  familyName("Liam")
  familyName("Jenny")
  familyName("Anja")
}
Result:

Hello Liam Refsnes
Hello Jenny Refsnes
Hello Anja Refsnes


Return Values
If you want the function to return a value, you need to define the data type of the return value (such as int, string, etc), and also use the return keyword inside the function:

Syntax
func FunctionName(param1 type, param2 type) type {
  // code to be executed
  return output
}
Function Return Example
Example
Here, myFunction() receives two integers (x and y) and returns their addition (x + y) as integer (int):

package main
import ("fmt")

func myFunction(x int, y int) int {
  return x + y
}

func main() {
  fmt.Println(myFunction(1, 2))
}
Result:

3

