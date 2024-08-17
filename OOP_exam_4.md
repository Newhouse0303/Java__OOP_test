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
        // the actual game event is initialised here. The description being a bit vague I'm not sure what a game entails but
        // I would opt for creating an abstract class GameEvent to be extended by different SubGames (TwoPlayerGameEvent, TeamGameEvent, etc.) Then upon
        // their creation current environment (weather, terrain, timeOfDay) data would be logged (and possibly updated during the game)
        // and the Player attributes would be updated accordingly.
        
    }
```

```
class UserInterface {

    // interaction is done via command line but the class can be easily modified to accomodate web-based graphic UI.
    // the class asks user the specs for creating a player and delegates the task to the PlayerManager
    // once the Player is created the user is informed and asked to enter a command to start the game
    // once the command ( or later 'click' ) is received the `newGame.play()` method of the class Game is called
}
```

class PlayerManager is responsible for creating new players based on user input. 
If storing existing players were rquired it would also take care of that. 


```
class PlayerManager {
    createPlayer( { userInput to match the class Player fields } ) {
        // the type defined by the user would be used to determine which subclass is used
        Player newPlayer = new {DesiredType}Player( { @params } )

}
```

The players a modeled with an `abstract class Player`, which holds the fields (health, attack power, defense, speed, superpower , name etc.) and methods `move()`, `attack()`, `fight()`, `die()` etc. shared by all types of players . Each player type has their own subclass `class {type here} extends Player`. The subclasses have additional fields for type-specific features. The mothods from the super are overridden according to the types' abilities 
and some additional methods


```
abstract class Player implements Combat {
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
The combats are modelled through abstract interface Combat which servers as a super for subinterfaces like `Duel`, `GroupBattle`, `Roast` etc. 
```
interface Combat {
    // reduces one heath point
    void reduceHealt(1);
}

interface GroupBattle {

    // group battle -specific methods 

}
