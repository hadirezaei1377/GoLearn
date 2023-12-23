API (application programming interface) is a way for two or more computers or services or front to back to communicate with each other.
it take place by URLs
API is a standard that everything must follow that.

JSON is like maps in golang, every thing have key and related value
it might we have two types for keys and values.

first step to call the API, its being as a client:
func main() {
    Client := &http.Client{}
    resp, err := client.Get("https://dummyjson.com/products")   // every url is a get request, resp has a lot of data
    if err != nil {
		fmt.Println(err)
	}
defer resp.Body.Close()
	response := &Response{} // response has a body, 
	json.NewDecoder(resp.Body).Decode(response)
	fmt.Printf("%#v\n", response.Products[0].Title)
}

tip:
type A interface {
    B C
}
b is a method that returns c , c is not type



<!-- 


type Product struct {
	ID                 int
	Title              string
	Description        string
	Price              int
	DiscountPercentage float32
	Rating             float32
	Stock              int
	Images             []string
}

type Response struct {
	Products []Product
	Total    int
	Skip     int
	Limit    int
} -->


	
