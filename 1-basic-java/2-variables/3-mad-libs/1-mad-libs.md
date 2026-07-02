## Java Variables: Mad Libs

In this project, we’ll use Java to write  a Mad Libs word game! Mad Libs have short stories with blank spaces that a player can fill in. The result is usually funny (or strange).

Mad Libs require:
* A short story with blank spaces (asking for different types of words).
* Words from the player to fill in those blanks.

“Roses are Red” poem example:

**MadLibs.java**
```java
public class MadLibs {
  /*
  Your description here
  */
  public static void main(String[] args){
    
    
    
    //The template for the story
    String story = "This morning "+name1+" woke up feeling "+adjective1+". 'It is going to be a "+adjective2+" day!' Outside, a bunch of "+noun1+"s were protesting to keep "+noun2+" in stores. They began to "+verb1+" to the rhythm of the "+noun3+", which made all the "+noun4+"s very "+adjective3+". Concerned, "+name1+" texted "+name2+", who flew "+name1+" to "+place1+" and dropped "+name1+" in a puddle of frozen "+noun5+". "+name1+" woke up in the year "+number+", in a world where "+noun6+"s ruled the world.";
  }       
}
```

SOLUTION:
1. Let’s create a comment that describes the program!

    The ```/*``` and ```*/``` are already in place for you. In between them, write a description that looks something like:

    ```git
    This program generates a mad libbed story.
    Author: Laura
    Date: 2/19/2049
    ```

    MadLibs.java
    ```java
    public class MadLibs {
        /*
        Your description here
        */
        public static void main(String[] args){
            
            /*
            This program generates a mad libbed story.
            Author: Laura
            Date: 2/19/2049
            */
            
            //The template for the story
            String story = "This morning "+name1+" woke up feeling "+adjective1+". 'It is going to be a "+adjective2+" day!' Outside, a bunch of "+noun1+"s were protesting to keep "+noun2+" in stores. They began to "+verb1+" to the rhythm of the "+noun3+", which made all the "+noun4+"s very "+adjective3+". Concerned, "+name1+" texted "+name2+", who flew "+name1+" to "+place1+" and dropped "+name1+" in a puddle of frozen "+noun5+". "+name1+" woke up in the year "+number+", in a world where "+noun6+"s ruled the world.";
        }       
    }
    ```

2. reading

3. The story that we have provided is going to need a protagonist.

    Create a String called ```name1``` that stores the name of the main character.

    ```java
    public class MadLibs {
        /*
        Your description here
        */
        public static void main(String[] args){
            
            /*
            This program generates a mad libbed story.
            Author: Jose Pardo
            Date: 07/02/2026
            */

            String name1 = "Jose Pardo";
            
            //The template for the story
            String story = "This morning "+name1+" woke up feeling "+adjective1+". 'It is going to be a "+adjective2+" day!' Outside, a bunch of "+noun1+"s were protesting to keep "+noun2+" in stores. They began to "+verb1+" to the rhythm of the "+noun3+", which made all the "+noun4+"s very "+adjective3+". Concerned, "+name1+" texted "+name2+", who flew "+name1+" to "+place1+" and dropped "+name1+" in a puddle of frozen "+noun5+". "+name1+" woke up in the year "+number+", in a world where "+noun6+"s ruled the world.";
        }       
    }
    ```

4. You will need to provide three adjectives.

    Create three Strings, ```adjective1```, ```adjective2```, and ```adjective3``` and store different adjectives in them.

    ```java
    public class MadLibs {
        /*
        Your description here
        */
        public static void main(String[] args){
            
            /*
            This program generates a mad libbed story.
            Author: Jose Pardo
            Date: 07/02/2026
            */

            String name1 = "Jose Pardo";
            String adjective1 = "happy";
            String adjective2 = "great";
            String adjective3 = "cool";

            //The template for the story
            String story = "This morning "+name1+" woke up feeling "+adjective1+". 'It is going to be a "+adjective2+" day!' Outside, a bunch of "+noun1+"s were protesting to keep "+noun2+" in stores. They began to "+verb1+" to the rhythm of the "+noun3+", which made all the "+noun4+"s very "+adjective3+". Concerned, "+name1+" texted "+name2+", who flew "+name1+" to "+place1+" and dropped "+name1+" in a puddle of frozen "+noun5+". "+name1+" woke up in the year "+number+", in a world where "+noun6+"s ruled the world.";
        }       
    }
    ```

5. You’ll also need to provide one verb.

    Create a String called ```verb1``` and store a verb in it.

    ```java
    public class MadLibs {
        /*
        Your description here
        */
        public static void main(String[] args){
            
            /*
            This program generates a mad libbed story.
            Author: Jose Pardo
            Date: 07/02/2026
            */

            String name1 = "Jose Pardo";

            String adjective1 = "happy";
            String adjective2 = "great";
            String adjective3 = "cool";

            String verb1 = "go";

            //The template for the story
            String story = "This morning "+name1+" woke up feeling "+adjective1+". 'It is going to be a "+adjective2+" day!' Outside, a bunch of "+noun1+"s were protesting to keep "+noun2+" in stores. They began to "+verb1+" to the rhythm of the "+noun3+", which made all the "+noun4+"s very "+adjective3+". Concerned, "+name1+" texted "+name2+", who flew "+name1+" to "+place1+" and dropped "+name1+" in a puddle of frozen "+noun5+". "+name1+" woke up in the year "+number+", in a world where "+noun6+"s ruled the world.";
        }       
    }
    ```

6. The story also needs six nouns.

    Create six **Strings**, ```noun1```, ```noun2```, ```noun3```, ```noun4```, ```noun5```, and ```noun6``` and initialize them to your favorite nouns.

    ```java
    public class MadLibs {
        /*
        Your description here
        */
        public static void main(String[] args){
            
            /*
            This program generates a mad libbed story.
            Author: Jose Pardo
            Date: 07/02/2026
            */

            String name1 = "Jose Pardo";

            String adjective1 = "happy";
            String adjective2 = "great";
            String adjective3 = "cool";

            String verb1 = "go";

            String noun1 = "people";
            String noun2 = "ambiental";
            String noun3 = "song";
            String noun4 = "place";
            String noun5 = "cold";
            String noun6 = "duck";

            //The template for the story
            String story = "This morning "+name1+" woke up feeling "+adjective1+". 'It is going to be a "+adjective2+" day!' Outside, a bunch of "+noun1+"s were protesting to keep "+noun2+" in stores. They began to "+verb1+" to the rhythm of the "+noun3+", which made all the "+noun4+"s very "+adjective3+". Concerned, "+name1+" texted "+name2+", who flew "+name1+" to "+place1+" and dropped "+name1+" in a puddle of frozen "+noun5+". "+name1+" woke up in the year "+number+", in a world where "+noun6+"s ruled the world.";
        }       
    }
    ```

7. Our story needs another character. Declare a String variable called ```name2``` and initialize it to the value of another name.

    ```java
    public class MadLibs {
        /*
        Your description here
        */
        public static void main(String[] args){
            
            /*
            This program generates a mad libbed story.
            Author: Jose Pardo
            Date: 07/02/2026
            */

            String name1 = "Jose Pardo";

            String adjective1 = "happy";
            String adjective2 = "great";
            String adjective3 = "cool";

            String verb1 = "go";

            String noun1 = "people";
            String noun2 = "ambiental";
            String noun3 = "song";
            String noun4 = "place";
            String noun5 = "cold";
            String noun6 = "duck";

            String name2 = "Andrea R.";

            //The template for the story
            String story = "This morning "+name1+" woke up feeling "+adjective1+". 'It is going to be a "+adjective2+" day!' Outside, a bunch of "+noun1+"s were protesting to keep "+noun2+" in stores. They began to "+verb1+" to the rhythm of the "+noun3+", which made all the "+noun4+"s very "+adjective3+". Concerned, "+name1+" texted "+name2+", who flew "+name1+" to "+place1+" and dropped "+name1+" in a puddle of frozen "+noun5+". "+name1+" woke up in the year "+number+", in a world where "+noun6+"s ruled the world.";
        }       
    }
    ```

8. Our story requires one number. Declare an ```int``` variable called ```number``` and set it to any whole number you like.

    ```java
    public class MadLibs {
        /*
        Your description here
        */
        public static void main(String[] args){
            
            /*
            This program generates a mad libbed story.
            Author: Jose Pardo
            Date: 07/02/2026
            */

            String name1 = "Jose Pardo";

            String adjective1 = "happy";
            String adjective2 = "great";
            String adjective3 = "cool";

            String verb1 = "go";

            String noun1 = "people";
            String noun2 = "ambiental";
            String noun3 = "song";
            String noun4 = "place";
            String noun5 = "cold";
            String noun6 = "duck";

            String name2 = "Andrea R.";

            int number = 2040;

            //The template for the story
            String story = "This morning "+name1+" woke up feeling "+adjective1+". 'It is going to be a "+adjective2+" day!' Outside, a bunch of "+noun1+"s were protesting to keep "+noun2+" in stores. They began to "+verb1+" to the rhythm of the "+noun3+", which made all the "+noun4+"s very "+adjective3+". Concerned, "+name1+" texted "+name2+", who flew "+name1+" to "+place1+" and dropped "+name1+" in a puddle of frozen "+noun5+". "+name1+" woke up in the year "+number+", in a world where "+noun6+"s ruled the world.";
        }       
    }
    ```

9. There’s one more variable! Declare a String called ```place1``` and store any place in it. This could be a city, or a town, or a country, or a planet!

    ```java
    public class MadLibs {
        /*
        Your description here
        */
        public static void main(String[] args){
            
            /*
            This program generates a mad libbed story.
            Author: Jose Pardo
            Date: 07/02/2026
            */

            String name1 = "Jose Pardo";

            String adjective1 = "happy";
            String adjective2 = "great";
            String adjective3 = "cool";

            String verb1 = "go";

            String noun1 = "people";
            String noun2 = "ambiental";
            String noun3 = "song";
            String noun4 = "place";
            String noun5 = "cold";
            String noun6 = "duck";

            String name2 = "Andrea R.";

            int number = 2040;

            String place1 = "San Isidro";

            //The template for the story
            String story = "This morning "+name1+" woke up feeling "+adjective1+". 'It is going to be a "+adjective2+" day!' Outside, a bunch of "+noun1+"s were protesting to keep "+noun2+" in stores. They began to "+verb1+" to the rhythm of the "+noun3+", which made all the "+noun4+"s very "+adjective3+". Concerned, "+name1+" texted "+name2+", who flew "+name1+" to "+place1+" and dropped "+name1+" in a puddle of frozen "+noun5+". "+name1+" woke up in the year "+number+", in a world where "+noun6+"s ruled the world.";
        }       
    }
    ```

10. READING 

11. Time to read the story! Use ```System.out.println()``` to print the ```story``` variable.

    ```java
    public class MadLibs {
        /*
        Your description here
        */
        public static void main(String[] args){
            
            /*
            This program generates a mad libbed story.
            Author: Jose Pardo
            Date: 07/02/2026
            */

            String name1 = "Jose Pardo";

            String adjective1 = "happy";
            String adjective2 = "great";
            String adjective3 = "cool";

            String verb1 = "go";

            String noun1 = "people";
            String noun2 = "ambiental";
            String noun3 = "song";
            String noun4 = "place";
            String noun5 = "cold";
            String noun6 = "duck";

            String name2 = "Andrea R.";

            int number = 2040;

            String place1 = "San Isidro";

            //The template for the story
            String story = "This morning "+name1+" woke up feeling "+adjective1+". 'It is going to be a "+adjective2+" day!' Outside, a bunch of "+noun1+"s were protesting to keep "+noun2+" in stores. They began to "+verb1+" to the rhythm of the "+noun3+", which made all the "+noun4+"s very "+adjective3+". Concerned, "+name1+" texted "+name2+", who flew "+name1+" to "+place1+" and dropped "+name1+" in a puddle of frozen "+noun5+". "+name1+" woke up in the year "+number+", in a world where "+noun6+"s ruled the world.";

            System.out.println(story);

        }       
    }
    ```

    OUTPUT:
    ```git
    This morning Jose Pardo woke up feeling happy. 'It is going to be a great day!' Outside, a bunch of peoples were protesting to keep ambiental in stores. They began to go to the rhythm of the song, which made all the places very cool. Concerned, Jose Pardo texted Andrea R., who flew Jose Pardo to San Isidro and dropped Jose Pardo in a puddle of frozen cold. Jose Pardo woke up in the year 2040, in a world where ducks ruled the world.
    ```