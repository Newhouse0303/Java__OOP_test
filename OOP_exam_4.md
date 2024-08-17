## 4 
The game starts by running the main class App. 
```
class App {
    Game newGame = new Game(); 
}
```
The constructor calls `run()` which prompts the UI
    
class Game {
    public Game() {
    run();

    void run() 



        
}

class UserInterface {}
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

