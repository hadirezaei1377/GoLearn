array and slice are two data type in golang.

array: They keep a set of information in themselves. For example, ten different strings or ten different numbers.
They are fixed type, that is, if the capacity is known at the beginning, it can store less than that, but not more.

for example:
func main() {
    array := [2]string{"Hadi","Khashayar"}
}

slice: flexible arrays
It has a flexible capacity and they take any number
for example:
func main() {
    slice := []string{"Hadi","Khashayar"}
}

Slices have a subset representation in which values are stored.
The slices point to that array.
If the capacity of the slice increases compared to the initial size, this array will be changed.
If the capacity of the slice is reduced compared to the original size, this array will not change.
The slices are pointers.
func main() {
    slice := []int{1, 2, 3} // initial
    slice = append(slice, 5)
}

Understanding the length of a slice:
func main() {
    slice := []int{1, 2, 3} // initial
    slice = append(slice, 5)
    fmt.Println(len(slice)) // output : 4 
}

Understanding the capasity of a underlying array:
len(slice)

Slices and arrays are numbered from zero,  array := [2]string{"Hadi","Khashayar"} Hadi is 0 and Khashayar is first

Access to indexes:
func main() {
    slice := []int{1, 2, 3} // initial
    slice = append(slice, 5)
    fmt.Println(slice[0]) // output : 1
}


Dividing a slice into smaller slices:
func main() {
    slice := []string{"Hadi","Khashayar", "Ali", "Ardeshir"}
    fmt.Println(slice[1:3]) // output : Khashayar and Ali
}

















