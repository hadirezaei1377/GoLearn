see this example :

func main(){
    number := 2

    fmt.Println(number)
    makeTwice(number)
    fmt.Println(number) 
}

func MakeTwice(number int) {
    number *= 2
}

output :
2
2

func main(){
    number := 2

    fmt.Println(number)  // first thing in print
    makeTwice(number)
    fmt.Println(number)  // third thing in print
}

func MakeTwice(number int) {
    number *= 2
    fmt.Println(number)   // second thing in print
}

output:
2
4
2

here we passed to makeTwice function just a copy of variable(2)
makeTwice function gets a copy and douplicates that and print the copy, after that this copy be deleted
any changes in this function occured on the copy not the main value

for having better results we can use reasign for number

func main(){
    number := 2

    fmt.Println(number)  
   number :=  makeTwice(number)
    fmt.Println(number)  
}

func MakeTwice(number int)int {
    number *= 2
    return number 
}

it was pass by value way to do the work correctly.
in this way we pass the value to functions, variables, custom types ...


pass by reference way:
take a zipcode of a house, we can use this zipcode every where, this address be copied every where and every time we want, but the house doesnt copy, we can use its address 
zipcode is a pointer that points to main value(in ram)
we pass this pointer every where we want and the changes be updated.

& this object creates a pointer to the value
* this object has two applications, sometimes check the value and sometimes tells us the type of value is pointer

func main(){
    number := 2

    fmt.Println(number)  
    makeTwice(&number)  // creates a pointer of this variable(number), number was int but now is a pointer, pointer to int(*int )
    fmt.Println(number)  
}

func MakeTwice(number *int)int {  // number *int means number is pointer to main value in ram that it is int
    *number *= 2
}

output:
2
4

see this example

type Car struct{
    Color string
    Power int
    mode bool
}

 func main(){
     bmw := Car{}

     bmw.Mode = true
     bmw.Drive()
 }

 func (c Car) Drive() {
    if c.Mode{
    fmt.Println("car is driving")
    }else{
        fmt.Println("first, turn on the car")
    }
}

make better this block of code:

func main(){
     bmw := Car{}

     bmw.Start()
     bmw.Drive()
}

func(c Car) Start(){
    c.Mode = true
}

output:
first, turn on the car

it means our mode doesnt work, because c is a copy of car(bmw)
in start function we have car is driving but the lifecycle of c finished after closing this function

resolve:

func(c *Car) Start(){
   (*c).Mode = true
}

it is equil to :

func(c *Car) Start(){
   c.Mode = true
}

 




