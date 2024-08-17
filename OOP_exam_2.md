
## 2.      

Saara Uusitalo

a) Polymorphism is evident in the way super class `Exception` is extended by `AIexception` and further `DataProcessingError` and
`ModelTrainingError`. As the main method catches all of them the program is expected to run smoothly. The difference between pipelines 1 and 2 
is the latter can throw AIexception the source of the might me more difficult to define, whereas the former specifies the error options in the 
signature and asiigns them to indvidual incidents in the code. In larger codebases more specific error handling can help identifying the problem. 

b) The code does its job but the use of Object in the signature is redundant as `@param double amount` * x is always double and using Object to create generics is a bad idea in any case. It could also work better if the values were dynamic. Appropriate error handling instead of `default -> amount * 2` would make more sense. The naming of `SpecificCurrencyConverter` could be more descriptive and all the cases could be created by implementing interfaces instead of big fat switch statement which would make it easier to add new currencies. 
