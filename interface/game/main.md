func main() {
    // create players
     cat := gamepkg.NewCat("Binky")
     dog := gamepkg.NewDog("Axlie")
     owl := gamepkg.NewOwl("Hanna")

     game := gamepkg.New(50) // create the game

     // joining to game
     game.Join(cat)
     game.Join(dog)
     game.Join(owl)

    var Winner gamepkg.Player
    for winner == nil{ //empty at first, loop until it be full
        game.MovePlayers()
        winner = game.CheckWinner()
        game.PrintBoard()
    }
    fmt.Printf("%s won the game!, winner.Name())
}