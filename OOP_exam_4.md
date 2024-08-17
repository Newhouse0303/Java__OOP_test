## 4 
The game starts by running the main class App. 
```
class App {
    Game newGame = new Game(); 
}
```
The constructor calls `run()` which prompts the UI

```
    
class Game {
    public Game() {
        run();

    public void run() {
        UserInterface.displayUI();
    }
    public void play() {
        
        
    }
```
```
class UserInterface {

    // here the interaction is done via command line but the class can be easily modified to accomodate web-based graphic UI.
    // the class asks user the specs for creating a player and delegates the task to the PlayerManager
    // once the Player is created the user is informed and asked to start the game which calls the `newGame.play()` method
}
```

class PlayerManager is responsible for creating new players based on user input. If storing existing players were rquired it would also take care of that. 

```
class PlayerManager {
    createPlayer( { userInput to match the class Player fields } ) {
        // the type defined by the user would be used to determine which subclass is used
        Player newPlayer = new {DesiredType}Player( { @params } )

}
```


class environmentManager {}
class combatManagers {}
```
The players a modeled with an `abstract class Player`, which holds the fields (health, attack power, defense, speed, superpower , name etc.) and methods `move()`, `attack()`, `fight()`, `die()` etc. shared by all types of players . Each player type has their own subclass `class {type here} extends Player`. The subclasses have additional fields for type-specific features. The mothods from the super are overridden according to the types' abilities 
and some additional methods
```
abstract class Player {
    int heath;
    int attackPower;
    int / String defence; 
    int speed;
    String superPower;

    // getters and setters
    // skeletons of `move()`, `attack()`, `fight()`, `die()`
}

class {SpecificPlayer} extends Player {
    // additional fields

    public SpecificPlayer( { fields from absract class Player } ) {
          this.health = health; etc..

    @Overriden methods from Player
    // additional methods
}

```
