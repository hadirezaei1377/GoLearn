a set of key(any type)-value(any type) pairs
For example, we have a store where we use maps to store product prices:

func main() {
    products := map[string]int {// keys are string(name of things) and values(the prices) are int
    "shoes": 150,
    "coat": 200,
    "socks": 2,
    "hat": 5,  
    }
    // Access to one of the values of this map:
    price, ok := products["shoes"] // we passed key to its value
    if ok {
        fmt.Println(price)
    }
}
// ok is a boolean value that shows us the key is exists or not , its optional

work with maps and loops:
write a function that gets string as input and counts the numbers of characters

func Count(str string) map[string]int{
    characters := map[string]int{} // characters is a map

    for _, char := range str{
        if _, ok := characters[string(char)]; != ok {
        characters[string(char)] = 0
        }
        characters[string(char)]++
    }
    return characters
}

func main(){
    str := "Hello world!"
    count := Count(str)
    fmt.Println(count)
}