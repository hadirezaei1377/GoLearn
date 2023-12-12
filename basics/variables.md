Golang is a static type programming language and its type must be known when defining a variable.
The variable type does not change during the program.

The variable definition is like this:
var + name + type + initial amount
var age int = 10
var last name string = "Hadi"
Assigning the initial value to the variable is optional, the topic of zero values is used here.
If there is an initial value, you can not define the type of the variable.
var name string = "hadi"
var name = "hadi"
var name string // zero value
If we use the var keyword, we can define the variable outside the main function
But := is used only inside the functions.
func main() {
    name := "hadi"
    age := 25
}

Basic types for variable definition:
string
float
bool
signed int // for example -10 - 10
unsigned int // for example 0 - 10
complex
byte // alias for the unsigned integer 8 type ( uint8 )
rune // alias for int32

Composite types for variable definition:
1- reference types
2- non-reference types
3- interface

reference types like function, pointer, slice, map and channel
non-reference types like array and struct

Variables have a fixed type, but their value can be changed, but constants also have a fixed value.
const name = "hadi"
