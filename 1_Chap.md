# Java Basics — Simple Detailed Notes

## 1. What is Java?

Java is a **high-level, object-oriented programming language** used to develop many types of applications.

Java can be used to create:

* Web applications
* Mobile applications
* Desktop applications
* Banking applications
* Enterprise applications
* Backend applications
* Cloud applications
* Games

Java was developed by **Sun Microsystems** and released in **1995**.

### Simple definition

> Java is a programming language that allows developers to write applications that can run on different platforms.

---

# 2. Why is Java Popular?

Java has many important features.

## 2.1 Simple

Java is relatively easy to learn and has a clear syntax.

Example:

```java
System.out.println("Hello World");
```

Output:

```text
Hello World
```

---

## 2.2 Object-Oriented

Java is based on **Object-Oriented Programming (OOP)**.

Important OOP concepts include:

* Class
* Object
* Encapsulation
* Inheritance
* Polymorphism
* Abstraction

These concepts help us organize large programs.

---

## 2.3 Platform Independent

Java follows the idea:

> **Write Once, Run Anywhere (WORA)**

A Java program can run on different operating systems when the appropriate JVM is available.

For example:

```text
Windows
Linux
macOS
```

---

## 2.4 Secure

Java provides several security features.

For example:

* No direct pointer manipulation like C/C++
* Runtime checks
* Managed memory
* Strong type checking

---

## 2.5 Robust

Robust means **reliable**.

Java provides features such as:

* Exception handling
* Automatic memory management
* Strong type checking

These help create reliable applications.

---

## 2.6 Multithreaded

Java supports **multithreading**.

This allows a program to perform multiple tasks concurrently.

For example:

```text
Download a file
       +
Play music
       +
Update the screen
```

---

## 2.7 High Performance

Modern Java applications can be very fast.

The **JIT (Just-In-Time) compiler** helps improve Java execution performance.

---

# 3. Java Editions

## Java SE

Java SE means:

> **Java Standard Edition**

It provides the core Java features.

Examples:

* Variables
* Data types
* Classes
* Objects
* Collections
* Exception handling
* Threads

It is the main edition beginners learn first.

---

## Jakarta EE

Jakarta EE is used for **enterprise applications**.

Examples:

* Banking systems
* Large business applications
* Enterprise web applications

It was previously known as **Java EE**.

---

## Java ME

Java ME means:

> **Java Micro Edition**

It was designed for smaller devices and embedded environments.

---

# 4. Java Environment

Three important terms are:

```text
JDK
JRE
JVM
```

These are extremely important in Java.

---

# 5. JVM

JVM means:

> **Java Virtual Machine**

The JVM executes **Java bytecode**.

The basic process is:

```text
Java Program
     ↓
Java Compiler
     ↓
Bytecode
     ↓
JVM
     ↓
Execution
```

The JVM is different for different operating systems.

For example:

```text
Windows → Windows JVM
Linux   → Linux JVM
macOS   → macOS JVM
```

---

# 6. Bytecode

Suppose we create:

```text
Hello.java
```

The Java compiler converts it into:

```text
Hello.class
```

The `.class` file contains **bytecode**.

The complete process is:

```text
Hello.java
     ↓
Java Compiler
     ↓
Hello.class
     ↓
Bytecode
     ↓
JVM
     ↓
Program runs
```

---

# 7. JRE

JRE means:

> **Java Runtime Environment**

JRE provides the environment required to **run Java applications**.

Conceptually:

```text
JRE
 ├── JVM
 └── Java Libraries
```

Simple meaning:

> **JRE is used for running Java applications.**

---

# 8. JDK

JDK means:

> **Java Development Kit**

JDK is used to **develop Java applications**.

It contains development tools, Java libraries, and runtime components.

Conceptually:

```text
JDK
 ├── Development Tools
 ├── Java Libraries
 └── JVM
```

One important development tool is:

```text
javac
```

which is the Java compiler.

---

# 9. JDK vs JRE vs JVM

Remember:

```text
JDK
 └── JRE
      └── JVM
```

### JVM

Runs Java bytecode.

### JRE

Provides the environment required to run Java applications.

### JDK

Provides tools required to develop Java applications.

### Easy way to remember

```text
JDK = Develop
JRE = Run
JVM = Execute
```

---

# 10. Java Installation

To develop Java programs, you normally install a **JDK**.

After installation, important commands include:

```text
java
```

and:

```text
javac
```

---

# 11. `javac` vs `java`

These two commands are very important.

## `javac`

`javac` is used to **compile Java source code**.

Example:

```text
javac Hello.java
```

This produces:

```text
Hello.class
```

So:

```text
.java → .class
```

---

## `java`

`java` is used to **run a Java application/class**.

Example:

```text
java Hello
```

Normally, you specify the class name rather than:

```text
java Hello.class
```

Use:

```text
java Hello
```

---

# 12. Eclipse IDE

Eclipse is an:

> **Integrated Development Environment (IDE)**

An IDE provides tools that make programming easier.

Eclipse provides features such as:

* Code editor
* Syntax highlighting
* Error detection
* Code completion
* Debugging
* Project management
* Program execution

Instead of manually doing:

```text
Write code
   ↓
Open terminal
   ↓
Compile
   ↓
Find errors
   ↓
Run
```

an IDE provides many of these features in one application.

---

# 13. What does IDE mean?

IDE stands for:

> **Integrated Development Environment**

It combines several development tools into one software application.

---

# 14. First Java Program

The classic first Java program is:

```java
class HelloWorld {
    public static void main(String[] args) {
        System.out.println("Hello World");
    }
}
```

Output:

```text
Hello World
```

Now let's understand every part.

---

# 15. `class HelloWorld`

```java
class HelloWorld
```

`class` is a Java keyword.

`HelloWorld` is the name of the class.

So:

```java
class HelloWorld
```

means:

> Create a class named `HelloWorld`.

---

# 16. Curly Braces `{ }`

Example:

```java
class HelloWorld {

}
```

The curly braces define the **body of the class**.

Everything belonging to the class is written inside them.

---

# 17. `main()` Method

Inside the class we write:

```java
public static void main(String[] args)
```

The `main()` method is the **entry point of a normal Java application**.

In simple words:

> When Java starts the application, execution begins from the `main()` method.

---

# 18. `public`

```java
public
```

means the method can be accessed from outside the class.

The standard Java entry point is:

```java
public static void main(String[] args)
```

---

# 19. `static`

```java
static
```

means the method belongs to the class rather than requiring an object of the class to be created first.

The JVM can therefore call the `main()` method to start the application.

---

# 20. `void`

```java
void
```

means the method does not return a value.

For example:

```java
void display()
```

does not return an integer, string, or other value.

---

# 21. `String[] args`

```java
String[] args
```

means `args` is an array of strings.

It can contain **command-line arguments**.

For example:

```text
java HelloWorld India
```

The value:

```text
India
```

can be received through `args`.

For now, remember the standard form:

```java
public static void main(String[] args)
```

---

# 22. `System.out.println()`

Example:

```java
System.out.println("Hello World");
```

This prints text to the console.

Output:

```text
Hello World
```

### `System`

Provides access to system-related functionality.

### `out`

Represents the standard output stream.

### `println`

Prints the given information and moves to the next line.

Example:

```java
System.out.println("Hello");
System.out.println("World");
```

Output:

```text
Hello
World
```

---

# 23. Semicolon `;`

Java statements generally end with a semicolon.

Example:

```java
System.out.println("Hello");
```

The `;` indicates the end of the statement.

---

# 24. Complete Program Breakdown

```java
class HelloWorld {
    public static void main(String[] args) {
        System.out.println("Hello World");
    }
}
```

Think of it like this:

```text
class HelloWorld
       ↓
Create a class

main()
   ↓
Starting point of program

System.out.println()
   ↓
Print something

"Hello World"
   ↓
Text to print
```

Output:

```text
Hello World
```

---

# 25. First Java Program — Tryout

The hands-on activity helps you create and execute your first Java program.

Basic process:

```text
Create Java file
      ↓
Write code
      ↓
Save file
      ↓
Compile
      ↓
Run
      ↓
See output
```

Example:

```java
class HelloWorld {
    public static void main(String[] args) {
        System.out.println("Hello World");
    }
}
```

Compile:

```text
javac HelloWorld.java
```

Run:

```text
java HelloWorld
```

Output:

```text
Hello World
```

---

# 26. First Java Program Using Eclipse

In Eclipse, the process is easier.

```text
Open Eclipse
     ↓
Create Java Project
     ↓
Create Java Class
     ↓
Write program
     ↓
Save
     ↓
Run
```

Eclipse manages much of the compilation and execution process for you.

---

# 27. Java Project in Eclipse

A typical project can look conceptually like:

```text
MyProject
│
├── src
│    └── HelloWorld.java
│
└── JRE System Library
```

### `src`

Contains source code.

### `.java`

Contains Java source code.

### JRE/JDK libraries

Provide standard Java classes and functionality.

---

# 28. Execution of Java Programs

Suppose we have:

```text
HelloWorld.java
```

containing:

```java
class HelloWorld {
    public static void main(String[] args) {
        System.out.println("Hello World");
    }
}
```

What happens when we run it?

---

## Step 1: Source Code

You write:

```text
HelloWorld.java
```

This is called **source code**.

It is the code written by the programmer.

---

## Step 2: Compilation

The Java compiler:

```text
javac
```

compiles the source code.

```text
HelloWorld.java
       ↓
     javac
       ↓
HelloWorld.class
```

---

## Step 3: Bytecode

The `.class` file contains **bytecode**.

Bytecode is an intermediate form of code designed to be executed by the JVM.

---

## Step 4: JVM Loads the Class

When you execute:

```text
java HelloWorld
```

the JVM starts and loads the required class.

---

## Step 5: JVM Finds `main()`

The JVM looks for:

```java
public static void main(String[] args)
```

This is the entry point.

---

## Step 6: JVM Executes the Program

The JVM executes the bytecode.

Eventually this statement executes:

```java
System.out.println("Hello World");
```

Output:

```text
Hello World
```

---

# 29. Complete Java Execution Flow

Remember this diagram:

```text
          SOURCE CODE
       HelloWorld.java
              |
              | javac
              ↓
          BYTECODE
       HelloWorld.class
              |
              | JVM
              ↓
      Program Execution
              |
              ↓
            OUTPUT
       Hello World
```

This is one of the most important concepts in Java.

---

# 30. Compiler vs JVM

Do not confuse the compiler and JVM.

## Compiler

Command:

```text
javac
```

Converts:

```text
.java → .class
```

---

## JVM

Runs:

```text
.class / bytecode
```

So the complete process is:

```text
Java Source Code
       ↓
     javac
       ↓
    Bytecode
       ↓
      JVM
       ↓
   Execution
```

---

# 31. Compilation Error

A compilation error occurs while compiling the program.

Example:

```java
class Hello {
    public static void main(String[] args) {
        System.out.println("Hello")
    }
}
```

There is a missing semicolon:

```text
;
```

The compiler detects the error.

You must fix the code and compile again.

---

# 32. Compilation Error vs Runtime Error

These are different.

## Compilation Error

Occurs during compilation.

Example:

```java
System.out.println("Hello")
```

The semicolon is missing.

The compiler catches the problem.

---

## Runtime Error

The program compiles successfully but a problem occurs while it is running.

The general flow is:

```text
Source Code
    ↓
Compilation
    ↓
Successful
    ↓
Program Starts
    ↓
Problem Occurs
    ↓
Runtime Error / Exception
```

---

# 33. Platform Independence

This is one of the most important Java concepts.

Suppose you create:

```text
Student.java
```

You compile it:

```text
Student.java
      ↓
Student.class
```

The `.class` file contains Java bytecode.

That bytecode can be executed on different operating systems using the appropriate JVM.

For example:

```text
Windows
   ↓
Windows JVM
   ↓
Student.class
```

or:

```text
Linux
   ↓
Linux JVM
   ↓
Student.class
```

or:

```text
macOS
   ↓
macOS JVM
   ↓
Student.class
```

---

# 34. Why is Java Platform Independent?

Java source code is compiled into **platform-independent bytecode**.

The bytecode is then executed by a **platform-specific JVM**.

The flow is:

```text
Java Source
     ↓
Java Compiler
     ↓
Bytecode
     ↓
Platform-specific JVM
     ↓
Execution
```

Therefore:

> **Java is platform independent because Java programs are compiled into platform-independent bytecode, which is executed by a JVM designed for the particular platform.**

---

# 35. Platform-Independent vs Platform-Dependent

The important distinction is:

```text
Java Bytecode → Platform Independent
JVM           → Platform Dependent
```

For example:

```text
                Java Source
                     ↓
                  Compiler
                     ↓
                  Bytecode
                     ↓
             ┌───────┼───────┐
             ↓       ↓       ↓
         Windows    Linux   macOS
           JVM       JVM      JVM
             ↓       ↓       ↓
         Execution Execution Execution
```

The same bytecode can be used with appropriate JVM implementations.

---

# 36. Why is JVM Platform Dependent?

The JVM needs to communicate with the underlying operating system and hardware.

For example:

```text
Windows JVM
```

works with Windows.

```text
Linux JVM
```

works with Linux.

```text
macOS JVM
```

works with macOS.

Therefore, JVM implementations are platform-specific.

---

# 37. Important Terms

| Term                   | Simple Meaning                                               |
| ---------------------- | ------------------------------------------------------------ |
| Java                   | Programming language                                         |
| Source Code            | Code written by programmer                                   |
| `.java`                | Java source file                                             |
| Compiler               | Converts source code into bytecode                           |
| `javac`                | Java compiler command                                        |
| Bytecode               | Intermediate code stored in `.class` files                   |
| `.class`               | Compiled Java class file                                     |
| JVM                    | Executes Java bytecode                                       |
| JRE                    | Environment for running Java applications                    |
| JDK                    | Tools for developing Java applications                       |
| IDE                    | Software used to develop programs                            |
| Eclipse                | Java-capable IDE                                             |
| `main()`               | Standard entry point                                         |
| `System.out.println()` | Prints output                                                |
| Platform Independent   | Bytecode can run on different platforms with appropriate JVM |

---

# 38. Important Quiz Questions

## What is Java?

Java is a high-level, object-oriented programming language used to develop different types of applications.

---

## What is JVM?

JVM stands for **Java Virtual Machine**.

It executes Java bytecode.

---

## What is JDK?

JDK stands for **Java Development Kit**.

It provides tools required to develop Java applications.

---

## What is JRE?

JRE stands for **Java Runtime Environment**.

It provides the environment required to run Java applications.

---

## What does `javac` do?

`javac` compiles Java source code into bytecode.

```text
.java → .class
```

---

## What does `java` do?

`java` starts the Java runtime and runs a Java application/class.

---

## What is bytecode?

Bytecode is the intermediate code generated by the Java compiler and stored in `.class` files.

---

## Why is Java platform independent?

Because Java source code is compiled into platform-independent bytecode, and that bytecode can be executed by the appropriate platform-specific JVM.

---

## What is Eclipse?

Eclipse is an **Integrated Development Environment (IDE)** used for writing, compiling, debugging, and running Java programs.

---

## What is the `main()` method?

The `main()` method is the standard entry point of a Java application.

```java
public static void main(String[] args)
```

---

## What does `System.out.println()` do?

It prints information to the console and moves the cursor to the next line.

---

# 39. Most Important Things to Memorize

## JDK, JRE, JVM

```text
JDK
 ↓
Used for development

JRE
 ↓
Used for running applications

JVM
 ↓
Executes bytecode
```

Remember:

> **JDK = Develop**
> **JRE = Run**
> **JVM = Execute**

---

## Java Execution

```text
.java
  ↓
javac
  ↓
.class
  ↓
Bytecode
  ↓
JVM
  ↓
Execution
  ↓
Output
```

---

## Platform Independence

```text
Java Source
     ↓
   javac
     ↓
  Bytecode
     ↓
 ┌───┼────┐
 ↓   ↓    ↓
JVM JVM  JVM
 ↓   ↓    ↓
Win Linux macOS
```

Remember:

> **Bytecode is platform independent. JVM is platform dependent.**

---

# 40. 5-Minute Revision

If you have only a few minutes before the quiz, remember these:

```text
Java
 ↓
Programming Language

.java
 ↓
Source Code

javac
 ↓
Compiler

.class
 ↓
Bytecode

JVM
 ↓
Executes Bytecode

JRE
 ↓
Runtime Environment

JDK
 ↓
Development Kit

Eclipse
 ↓
IDE

main()
 ↓
Entry Point

System.out.println()
 ↓
Prints Output
```

## Most Important Flow

```text
.java
  ↓
javac
  ↓
.class / Bytecode
  ↓
JVM
  ↓
Execution
  ↓
Output
```
