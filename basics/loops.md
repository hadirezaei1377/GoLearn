We use loops when we want something to be repeated.

for example :
func main() {
    fmt.Println(Greeting("Hadi"))
    fmt.Println(Greeting("manoochehr"))
    fmt.Println(Greeting("Khashayar"))
    fmt.Println(Greeting("Sadra"))
}

func Greeting(name string) string {
    return "Hi" + name + ",wellcome to our website"
}

we have to better this code for a lots of numbers
in golang we have just for loop
we can write this loop in two main types :
1- for + key-value := range + items
Browse items for each key and value
Items can be a slice or array or map or channel and...
func main() {
    names := []string{"Hadi", "manoochehr", "Khashayar", "Sadra"}
    for index, name := range names { // index starts from 0
         fmt.Println(Greeting("name"))
    }
}

but we dont need index here so :
func main() {
    names := []string{"Hadi", "manoochehr", "Khashayar", "Sadra"}
    for _, name := range names { 
         fmt.Println(Greeting("name"))
    }
}

2- for + init + condition + increment
init happens once, but condition and increment happen for every round of the loop
Investigating the divisibility of the number 7 in a certain range of numbers :
func main() {
    for i := 1; i < 100; i++ {
if i % 7 == 0 {
    fmt.Println(i, "is divisible by 7")
}
    }
}

i := 1 is initialization
i < 100 is condition, if it is not correct, it will come out of the loop
increment changes the conditions for cancelling the loop

This loop can also become a while loop and an infinite loop