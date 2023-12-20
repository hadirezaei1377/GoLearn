here we define some shapes:

type Rectangle struct {
	Width  float64
	Height float64
}

type Circle struct {
	Radius float64
}

we want define a function for clculate the area of them:

func (r Rectangle) Area() float64 {
	return r.Width * r.Height
}

func (r Rectangle) Name() string {
	return "rectangle"
}

func (c Circle) Area() float64 {
	return math.Pi * math.Pow(c.Radius, 2)
}

func (c Circle) Name() string {
	return "circle"
}
 
we want to have another function that gets any shapes and calculates their area:
we have two types and any of them has their method for calculating the area, the shared properties here are name and area

so we define interface with expected parameters:

type Shape interface {
	Area() float64
	Name() string
}

interface just interactes with methods.

anything that have Area() and Name() is of interface type

func PrintArea(shape Shape) {
	fmt.Printf("Area of %s is %f\n", shape.Name(), shape.Area())
}
its no matter what we have here, its just important we takes a thing with area and name

check it,

func main() {
    circle := shape.Circle{Radius: 2}
    rectng := shape.Rectangle{Width: 3, Height: 4}

    PrintArea(circle)
    PrintArea(rectng)
}


 





