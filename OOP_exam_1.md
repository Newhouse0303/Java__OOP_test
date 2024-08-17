## Saara Uusitalo

## 1.
The main `class App` holds the private list of cards. The class card has private fields that are only accessible via setters and getters thus encapsulating the information. It is assumed
the the players are required to sign in and have an account. The accounts are instances of subclasses of ` class User` which are `class Player extends User ` and `class Admin extends User`.
The super class has the usual fields and a search and view methods for the list, which both subclasses inherit. `Admin` also has methods for adding, editing and deleting data from on the list.
These actions are done through `class CardManager` which is only accessed by the admin. 


```
class Card {
  String title;
  float cost;
  String type;
  int damage;

  // setters and getters 

abstract class User {
  String id;
  String name;

  // methods for rearching and viewing DB
  

class Player extends User {}

class Admin extends User {

  // includes additional methods for editing DB
} 
