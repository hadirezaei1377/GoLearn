A struct is like a template that we define how to fill.

func main(){
    var Person = struct{ // the properties of a person
           Name string
           Age int 
    }{ // passing data to struct
      "Hadi",
      32,
    }

}

so if we type person. we see after dot these cases person.Name and persno.Age
for a lot of people it will be a problem so we use custom types :

type Person struct{
    Name string
    Age int 
}

func main(){
    person := person {
        "Hadi",
        25,
    }
    person2 := person {
        "Khashayar",
        33,
    }
}

another example:

type Person struct{
    Name string
    Age int 
    Car Car
}

type Car struct{
    Color string
    Power int
    state bool
}

func main(){
    person := person {
        "Hadi",
        25,
    }
    person2 := person {
        "Khashayar",
        33,
    }
}