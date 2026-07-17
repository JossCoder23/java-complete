## What Is Serialization?

#### Learn what serialization is and why it’s useful.

So far, object-oriented programming (OOP) has made our code more modular and reusable with the use of objects. One of the benefits of using objects is the ability for them to encapsulate state (or data) to use within our program, but what if we wanted to store an object’s state in a file or send it over a network? As a matter of fact, we can do this by serializing our objects.

<img src="serialization.png" width="500">

Serialization describes the process of taking an object’s state and transforming it into a stream of bytes. Let’s discuss the terminology further:

* A stream is an abstract definition of a sequence of data that is made available over time.
* A byte is an 8 bit (0s or 1s) group of data.
* A stream of bytes is a sequence of bytes that is made available over time.

To serialize an object, its fields and their types are stored in the form of bytes. These bytes are then able to be written to memory, a file, a database, or sent over a network with all the information necessary to recreate the object.

### Deserialization

You may be wondering, “This is great and all but how do I get my object back from this stream of bytes?” This is where deserialization comes in.

Deserialization as the name suggests, does the opposite of serialization and converts a stream of bytes back into an object. Using both serialization and deserialization gives us the flexibility to persist our objects and get them back when needed.

There are a couple of important details to note about serialization and deserialization:

* The stream of bytes created by serialization only includes the member variables of an object and not its methods.
* Deserialization creates a copy of the original object. This copy shares the same state but is an entirely new object in memory.

Many programming languages like Java, C++, etc. support serialization and deserialization but differ in how they implement the process. Ultimately, this gives us the flexibility to work with the objects in, say Java, and also be able to work with a copy of that object in C++.