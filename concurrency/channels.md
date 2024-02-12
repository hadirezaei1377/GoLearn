channels can be considered like queues, 

func main() {
    myChannel := make(chan string, 100) // 100 is capacity of channels by default 0

    data := <-myChannel
    fmt.Println(data)
}

output is null 

func main() {
    myChannel := make(chan string, 100) 

    myChannel <- "Ali"
    myChannel <- "Reza"

    data := <-myChannel
    fmt.Println(data)
}

output :
Ali
Reza

we can also make  commiunication between gorutines by channel:

func main() {
    myChannel := make(chan string, 100) 

  go func() {
    <-time.After(time.second)
    myChannel <- "Reza"
  }

    data := <-myChannel
    fmt.Println(data)
}

output:
Ali 
Reza    // after one second