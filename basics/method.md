When we want to define a function for our custom types, we use methods.
for example :

type Car struct {
    Producer string
    Model string
    Color string
    Power int
    Mode bool
}

func main() {
    bmw_i8 := Car{
        Producer: "bmw",
        Model: "i8",
        Color: "white",
    }
      mc_720 := Car{
        Producer: "maclaren",
        Model: "720",
        Color: "black",
      }
}

// define methed: a functionablity for instance
// method can has inputs and outputs but it must has () before its name
func (c Car) Drive() {}  // c is a variable  and   car is the origion    Driva has a variable named c and we have access to it

func (c Car) Drive() {
    fmt.Println(c.Producer + "-" + c.Model, "is driving")
}
 
 func main(){
    bmw_i8.Drive()
 }

 check if the car is on can drive:

func (c Car) Drive() {
    if c.Mode{
    fmt.Println(c.Producer + "-" + c.Model, "is driving")
    }else{
        fmt.Println(c.Producer + "-" + c.Model, "cant be driven")
    }
}

 func main(){
     bmw_i8.Mode = true
     bmw_i8.Drive()
 }