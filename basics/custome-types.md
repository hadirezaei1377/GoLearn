custome types in golang must be created(fork) from known types
type is key 
type MyInt int 
we can assign some features to this type 
we usually combine this types by structs and interfaces or maps
for example :
type Grades map[string]int // for students mark

how we use it :
func main() {
    grades := Grades{
        "Hadi": 20,
        "khashayar": 19,
    }
}

