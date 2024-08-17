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

a) The suitable class construction could be nested class: the initial search would be done through creating an instance of `class Query` which would hold a nested class `SearchResults` which in the case in question would assemble and return the list. Nesting works here as the result does not exist without the query and whent the search is closed also the nested result object disappears. Separating the two functions (search and return) in different classes makes the code maintainable ( e.g. database keys are modified, different outputs are required for different purposes etc. ). 

b) The aforementioned `class Query` could have a method called `filter` which would take the List<Entry> and the filtering conditions as parameters. Depending on the overall complexity filter could also be an interface the `class Query` implements. This way different filter options could be added easily to complement the basic one which checks each Entry according to the condition and returns a boolean which is the used to put together a new filtered list. 

c) The trasactions could be modeled by using the record class. `record Trasaction` would contain all the important information such as type, value, currency, time etc. The attributes would then be used to create the correct output via `toString` method and the attributes could be accessed easily for transactions and comparision. The immutability of Record is no problem here as the by the time of logging the transactions they are no longer subject to change.



## 4. 
