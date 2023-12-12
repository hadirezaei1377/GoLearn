Functions take input and deliver output to us. we use functions to avoid repetitive tasks.
We have to call every function except the main function for it to work.

fmt.Println  : println is a function from fmt library 
definition: func fmt.Println(a ... any)(n int, err error) it gives anything and returns an int and an error
Sometimes functions don't need to use outputs like fmt.Println("Hi there!")

for example consider this :
func main() {
    fmt.Println("Hi Hadi, wellcome to our website")
}
it is a right code , but for more persons 
func main() {
    fmt.Println("Hi Hadi, wellcome to our website")
    fmt.Println("Hi manoochehr, wellcome to our website")
    fmt.Println("Hi Khashayar, wellcome to our website")
    fmt.Println("Hi Sadra, wellcome to our website")
    .
    .
    .
    .

}

its better to use this way :
we define a function for that, 
a function that recieves an input and returns an output
func Greeting(name string) string {
    return "Hi" + name + ",wellcome to our website"
}

so here our application :
func main() {
    fmt.Println(Greeting("Hadi"))
    fmt.Println(Greeting("manoochehr"))
    fmt.Println(Greeting("Khashayar"))
    fmt.Println(Greeting("Sadra"))
    .
    .
    .
    .

}

func Greeting(name string) string {
    return "Hi" + name + ",wellcome to our website"
}


We cannot combine two different types together,
for example :
func main() {
    fmt.Println(Greeting("Hadi", 25))
    fmt.Println(Greeting("manoochehr", 27))
    fmt.Println(Greeting("Khashayar", 32))
    fmt.Println(Greeting("Sadra", 19))
    .
    .
    .
    .

}

func Greeting(name string) string {
    return "Hi" + name + ",wellcome to our website" + age // its wrong
}

we have to use sprintf, it recievs arguments and return string
%s string
%d int
%v value // default format
%f float

modified application :
func main() {
    fmt.Println(Greeting("Hadi", 25))
    fmt.Println(Greeting("manoochehr", 27))
    fmt.Println(Greeting("Khashayar", 32))
    fmt.Println(Greeting("Sadra", 19))
    .
    .
    .
    .

}

func Greeting(name string, age int) string {
    return fmt.sprintf("Hi %s, you are %d years old, name , age)
}


