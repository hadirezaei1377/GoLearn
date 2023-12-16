type FuelTank struct{
     Capacity int
     Filled int 
}

// this method is used for filling the tank, so it will change the Filled from FuelTank struct, it must be a pointer

func (f *FuelTank) Fill() {  
    f.Filled = f.Capacity 
}

type Car struct{
    Color string
    Power int
    mode bool
    FuelTank FuelTank
}

/* 
when name of type be equil to name of attribute like FuelTank FuelTank, we can write:

type Car struct{
    Color string
    Power int
    mode bool
    FuelTank 
}

its wrong
type Car struct{
    Color string
    Power int
    mode bool
    Tank FuelTank
}
*/

func (c *car) FillTank (){
     c.FuelTank.Fill()
}

 func (c *Car) Drive() {
    if c.Mode{
    fmt.Println("car is driving")
    c.FuelTank.Filled -= 10
    }else{
        fmt.Println("car cant be driven whitout getting on")
    }
}

func main(){
    car := &car{}
    car.Start()
    car.Drive()
 }










