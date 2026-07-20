## Review

Great job! You’ve learned a lot about serialization.

In this lesson we’ve discussed how:

* Java makes serialization easy using the ```Serializable``` interface.
* The ```Serializable``` interface is a marker interface and requires no ```methods``` to be implemented.
* To use ```FileOutputStream``` and ```ObjectOutputStream``` to serialize objects to a file.
* To use ```FileInputStream``` and ```ObjectInputStream``` to deserialize objects from a file.
* ```static``` and ```transient``` fields are not serializable.
* The JVM handles serializing objects with reference type fields.
* To implement ```writeObject()``` to customize the serialization of an object to handle non-serializable fields.
* To implement ```readObject()``` to customize the deserialization of an object with non-serializable fields.

Knowing these topics will improve your mastery of Java and allow you to persist your objects past program termination or transport them over a network.