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
    * The file computerStorage.txt is created, although errors are written to the file, and Something went wrong… is printed to the terminal.
    * The file computerStorage.txt is created and Everything is good here! Serialization complete! is printed to the terminal.