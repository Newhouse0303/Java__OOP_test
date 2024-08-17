## Saara Uusitalo

## 1.
The main `class App` holds the private list of cards. The class card has private fields that are only accessible via setters and getters thus encapsulating the information. It is assumed
the the players are required to sign in and have an account. The accounts are instances of subclasses of ` class User` which are `class Player extends User ` and `class Admin extends User`.
The super class has the usual fields and a search and view methods for the list, which both subclasses inherit. `Admin` also has methods for adding, editing and deleting data from on the list.
These actions are done through `class Cardmanager` which is only accessed by the admin. 

The class card has private fields accessed via setters and getters. The only way to modify the database is through an `Admin` accounts methods which utilize the `Card` class's setter methods.

By creating separate user classes for player and admin, the database is secured from unexpected breaches. The admin can 

What principle of data protection would you choose in the case of the Card type when you want to serve the two different roles mentioned:

A player makes a search query and you want to offer the host a view that only supports reading the card listing.
Administrative staff want to permanently edit the information of a specific card.

Describe the mechanisms you choose and their consequences for class features, class invariant, and usage. It will suffice to focus mainly on the Card type. For simplicity, we can assume that the database is an array (Cards []) or a list (List[Cards]) of show hosts (you can choose either - lists should be familiar to you from previous courses). You may also implement the program if you wish, but just creating the specifications is enough.

```
class Card {
  String title;
  float cost;
  String type;
  int damage; 

```

