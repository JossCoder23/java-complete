# What Is an IDE?

### Learn about the Integrated Development Environment, an application that makes programming easier!

## What is an IDE?
An IDE, or Integrated Development Environment, enables programmers to consolidate the different aspects of writing a computer program.

IDEs increase programmer productivity by combining common activities of writing software into a single application: editing source code, building executables, and debugging.

## Editing Source Code
Writing code is an important part of programming. We start with a blank file, write a few lines of code, and a program is born! IDEs facilitate this process with features like syntax highlighting and autocomplete.

### Syntax Highlighting
An IDE that knows the syntax of your language can provide visual cues. Keywords, words that have special meaning like ```class``` in Java, are highlighted with different colors.

Compare these two code samples:
```git
// without syntax highlighting

public class NiceDay {
  public static void main(String[] args) {
    System.out.println("It's a nice day out!");
  }
}
```

```java
// with syntax highlighting

public class NiceDay {
  public static void main(String[] args) {
    System.out.println("It's a nice day out!");
  }
}

```

Syntax highlighting makes code easier to read by visually clarifying different elements of language syntax.

### Autocomplete
When the IDE knows your programming language, it can anticipate what you’re going to type next!

We’ve seen statements with ```System.out.println()``` quite a bit so far. In an IDE, we might see ```System``` as an autocomplete option after only typing ```Sy```. This saves keystrokes so the programmer can focus on logic in their code.

### Building Executables
Java is a compiled language. Before programs run, the source code of a .java file must be transformed into an executable .class by the compiler. Once compiled, the program can be run from the terminal.

This compilation process is necessary for every program, so why not have the IDE do it for us? IDEs provide automated build processes for languages, so the act of compiling and executing code is abstracted away, like in Codecademy lessons.

### Debugging
No programmer avoids writing bugs and programs with errors.

When a program does not run correctly, IDEs provide debugging tools that allow programmers to examine different variables and inspect their code in a deliberate way.

IDEs also provide hints while coding to prevent errors before compilation.