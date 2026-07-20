## Quiz

1. Review the following code and identify the correct output (assume each class is its own file):

    ```java
    /* File 1: Computer.java */ 
    import java.io.*;

    public class Computer implements Serializable {

        private static final long serialVersionUID = 1L;
        Keyboard keyboard;
        Monitor monitor;

        public static void main(String[] args) {
            Computer computer = new Computer();
            computer.keyboard = new Keyboard();
            computer.monitor = new Monitor();
            try {
            FileOutputStream fileOutputStream = new FileOutputStream("computerStorage.txt");
            ObjectOutputStream objectOutputStream = new ObjectOutputStream(fileOutputStream);
            objectOutputStream.writeObject(computer);
            } catch (IOException e) {
            System.out.println("Something went wrong...");
            }
            System.out.println("Everything is good here! Serialization complete!");
        }

    }


    /* File 2: Keyboard.java */ 
    import java.io.Serializable;

    public class Keyboard implements Serializable {
        private static final long serialVersionUID = 1L;
        String brand;
    }

    /* File 3: Monitor.java */ 
    public class Monitor {
        String brand;
        int size;
    }
    ```
    * The file computerStorage.txt is not created and Something went wrong… is printed to the terminal.
    * The code results in a compile-time error and won’t compile.
    * ```The file computerStorage.txt is created, although errors are written to the file, and Something went wrong… is printed to the terminal.```
    * The file computerStorage.txt is created and Everything is good here! Serialization complete! is printed to the terminal.

2. What two keywords will automatically prevent a field from not being serialized?
    * static and private
    * unserializable and private
    * final and transient
    * ```static and transient```

3. True or False: The output file when using FileOutputStream and ObjectOutputStream results in a human-readable file, similar to a poorly formatted JSON file.
    * ```False```
    * True

4. Fill in the code to properly implement the Serializable interface.
    ```java
    import java.io. ___________ ;

    public class Armour implements ___________ {

        /* Class Variables */
        private static final long ___________ = 1L;

        /* Instance Variables */
        private final String name;
        private int durability;
        private int defenseRating;

        /* Constructors */
        public Armour(String name, int durability, int defenseRating) {
            this.name = name;
            this.durability = durability;
            this.defenseRating = defenseRating;
        }

    }
    ```
    * Codable
    * ```serialVersionUID```
    * Savable
    * Cerealizable 
    * ```Serializable``` 
    * serialUID
    * ```Serializable```

5. In Java, we _____ objects that we need to persist, store in a file, or send over a network
    * stream
    * compress
    * ```serialize```
    * condense

6. Review the following code and identify the correct output (assume each class is its own file):

    ```java
    /* Computer.java */
    import java.io.*;

    public class Computer implements Serializable {
    private static final long serialVersionUID = 1L;
    Keyboard keyboard;
    Monitor monitor;

    public static void main(String[] args) {
        Computer computer = new Computer();
        computer.keyboard = new Keyboard();
        computer.monitor = new Monitor();
        try {
        FileOutputStream fileOutputStream = new FileOutputStream("computerStorage.txt");
        ObjectOutputStream objectOutputStream = new ObjectOutputStream(fileOutputStream);
        objectOutputStream.writeObject(computer);
        } catch (IOException e) {
        System.out.println("Something went wrong...");
        }
        System.out.println("Everything is good here! Serialization complete!");
    }
    }

    /* IODevices.java */
    import java.io.Serializable;

    public class IODevices implements Serializable {
        private static final long serialVersionUID = 1L;
    }

    /* Keyboard.java */
    public class Keyboard extends IODevices {
        String brand;
    }

    /* Monitor.java */
    public class Monitor extends IODevices {
        String brand;
        int size;
    }
    ```
    * The file computerStorage.txt is created, although errors are written to the file, and Something went wrong… is printed to the terminal.
    * An error is generated because there is no constructor for the Computer class.
    * ```Everything is good here! Serialization complete! is printed to the terminal and the computerStorage.txt file is created correctly.```
    * The code results in a compile-time error.

7. Fill in the correct helper classes and methods to read and write objects to a file.

    ```java
    import java.io.*;

    public class Computer implements Serializable {
        private static final long serialVersionUID = 1L;
        Keyboard keyboard;
        Monitor monitor;

        public static void main(String[] args) {
            Computer computer = new Computer();
            computer.keyboard = new Keyboard();
            computer.monitor = new Monitor();
            try {
            __________ fs = new __________("computerStorage.txt");
            ObjectOutputStream os = new ObjectOutputStream(fs);
            os.__________(computer);
            } catch (IOException e) {
            System.out.println("Something went wrong...");
            }

            computer = null;

            try {
            __________ fis = new __________("computerStorage.txt");
            ObjectInputStream ois = new ObjectInputStream(fis);
            computer = (Computer) ois. __________ ();
            } catch (IOException | ClassNotFoundException e) {
            System.out.println("Something went wrong...");
            }
        }
    }
    ```
    * deserializeObect
    * ```FileInputStream```
    * FileSystemOutputStream
    * serializeObject
    * ```FileInputStream```
    * ```readObject```
    * ```FileOutputStream```
    * FileSystemOutputStream
    * FileSystemInputStream
    * ```writeObject```
    * ```FileOutputStream```
    * FileSystemInputStream

8. Converting an object from its bytecode format back to its Java object format is called:
    * Conversion
    * ObjectInputStream
    * ObjectOutputStream
    * ```Deserialization```