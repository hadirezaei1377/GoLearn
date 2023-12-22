Why have we started learning Golang?

--Simplicity
--Absence of characteristics such as Inheritance
--Having limited keywords
--Having simple concurrency model
--Fast compilation
--Optimal memory
--High speed
--Growing community
--Backed by google



when we use go build instead go run we will have a .exe file, this file will be created beside the .go file and whenever we want to use it we should open it
but it be open for less than 1 second
we can use time sleep for example 5 seconds and see it but this way is wrong
we want show it forever
we can use for loop 
so in main function {
    for {
        get inputs
        calculate and print
    }
}

for getting inputs in terminal :
func main() {
    GetInput()
}

func GetInput() {
    var name string
     fmt.Scanln(&name)
     fmt.Println("welcome" + name)
}

so after go run in terminal
its waiting for entering inputs
we enter hadi
output: 
welcome hadi
so any name we entered here, it returns welcome name, the numbers is not important

func main() {
    GetInput()
}

func GetInput() {
    var name string
    fmt.Print("what is your name?")
    fmt.Scanln(&name)
    fmt.Println("welcome" + name)
}


