Decision making based on conditions and situations
For example, we store the result of the function in a variable
func Greeting(name string, age int) string {
    return fmt.sprintf("Hi %s, you are %d years old, name , age)
}

modified :
func Greeting(name string, age int) string {
    var result string
    if age < 12 {
        result = fmt.sprintf("Hi %s, you are a child, name)
    } else if age > 12 %% age < 20 { // and means  both conditions must be true
        result = fmt.sprintf("Hi %s, you are a teenager, name)
    } else { // Default
        result = return fmt.sprintf("Hi %s, you are %d years old, name , age)
    }
    
    return result
}

The use of else/if is used when the conditions are dependent on each other, that is, if the first condition is true, it does not check the other conditions.


a function to check divisibility:
// % This operator gives us the remainder of the division, 5 % 2 --> 1,  4 % 2 --< 0
func main() {

}

func IsDivisible(number, divisor int)bool{
if number%divisor == 0 {
    return true
}
return false // otherwise
}
tip: If the return is correct here, there is no need to check for false, so we don't need to use else/if.
In general, wherever we return in the functions, the functioning of the function ends and the rest of the code is not executed.

In the continuation of the function we defined:
func main(){
    fmt.PrintLn(IsDivisible(4,2)) // output: true
    fmt.PrintLn(IsDivisible(5,3)) // output: false
    fmt.PrintLn(IsDivisible(2,1)) // output: true
}  

another example for conditions:
divisible 
{
3 & not 5 --> fizz
5 & not 3 --> buzz
3 & 5 --> fizz-buzz
otherwise --> itself
}

func FizzBuzz(number int)string{
    if number % 3 == 0 && number % 5 != 0 {
        retuen "fizz"
    } else if number % 3 != 0 && number % 5 == 0 {
        return "buzz"
    } else if number % 3 == 0 && number % 5 == 0 {
        return "fizz-buzz"
    }
   return fmt.Sprint(number) // otherwise
}
// we used sprint because we have int and we have to print string