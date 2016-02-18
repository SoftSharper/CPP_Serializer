# CPP Serializer - Simple way to build serializable classes 

C++ wasn't developed with a mind of support for rich RTTI. The C++ compiler translates the code for the best of performance or compactness, but doesn’t leave any information about variables or class structures suitable for building any type of framework which can create a bridge between data storage and alive objects. Limited RTTI does’t provide any methods for enumeration of variables and class members or traversing through data structures. 

People of C++ make all kinds of efforts to easy serialization. We use BOOST, Cerial... But sometimes we want a simple mechanism based on the STL to make a draft of idea without pooling more code then C++ offers in TR2.

So, why can't we send our objects to stringstream and read them from there? 

First of all an executable knows little to nothing about data structures. C++ 11 provides scarce information about data types and classes at the run time and gives some information from virtual tables. But there is no such thing as "reflection" defined in the C++ specification. Therefore we have manually to list all members of the class and not forget to call serialization for the base classes.

This would be a half of problem and we can live with this if serialization can be implemented by clean and regular code, which can have a good readability and testability. Saying "testability" I mean it could be easy to create the unit tests to check serialization and it could be easy to note check if any field is messed in the serialization. 

Another half of this problem is coming from implementation of STL streams. Let check if we can use the STL streams to serialize and deserialize C++ basic types and STL containers.
