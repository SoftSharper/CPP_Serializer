# CPP Serializer - Simple way to build serializable classes 

C++ wasn't developed with a mind of support for rich RTTI. The C++ compiler translates the code for the best of performance or compactness of size, but doesn’t leave any information about variable or class structures suitable for building any type of framework which can create a bridge between data storage and alive objects. Limited RTTI does’t provide any methods for enumeration of data variables or traversing through data structures. We still love it.

People of C++ make all kinds of efforts to easy serialization. We use BOOST, Cerial... But sometimes we want a simple mechanism based on the STL to make a draft of idea without pooling more then TR2.

So, why can't we send our ojbects to stringstream and read them from there? 
