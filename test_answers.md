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

## 2.

a) Polymorphism is evident in the way super class `Exception` is extended by `AIexception` and further `DataProcessingError` and
`ModelTrainingError`. As the main method catches all of them the program is expected to run smoothly. The difference between pipelines 1 and 2 
is the latter can throw AIexception the source of the might me more difficult to define, whereas the former specifies the error options in the 
signature and asiigns them to indvidual incidents in the code. In larger codebases more specific error handling can help identifying the problem. 

b) The code does its job but the use of Object in the signature is redundant as `@param double amount` * x is always double and using Object to create generics is a bad idea in any case. It could also work better if the values were dynamic. Appropriate error handling instead of `default -> amount * 2` would make more sense. The naming of `SpecificCurrencyConverter` could be more descriptive and all the cases could be created by implementing interfaces instead of big fat switch statement which would make it easier to add new currencies. 

## 3. 



## 4. 
