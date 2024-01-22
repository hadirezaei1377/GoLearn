A condition can be either true or false.

Go supports the usual comparison operators from mathematics:

Less than <
Less than or equal <=
Greater than >
Greater than or equal >=
Equal to ==
Not equal to !=
Additionally, Go supports the usual logical operators:

Logical AND &&
Logical OR ||
Logical NOT !

	
Go has the following conditional statements:

Use if to specify a block of code to be executed, if a specified condition is true
Use else to specify a block of code to be executed, if the same condition is false
Use else if to specify a new condition to test, if the first condition is false
Use switch to specify many alternative blocks of code to be executed

The if Statement
Use the if statement to specify a block of Go code to be executed if a condition is true.

Syntax
if condition {
  // code to be executed if condition is true
}
Note that if is in lowercase letters. Uppercase letters (If or IF) will generate an error.
