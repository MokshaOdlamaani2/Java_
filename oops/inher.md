## Java Inheritance — `extends` and `super`

### 1. What is Inheritance?

Inheritance allows one class to acquire properties and methods of another class.

* **Parent/Base/Super class** → existing class
* **Child/Derived/Sub class** → new class that inherits

It helps in:

* Code reusability
* Method overriding
* Better organization

---

## 2. `extends` Keyword

Used to inherit a class.

### Syntax

```java
class Parent {
    // properties and methods
}

class Child extends Parent {
    // additional features
}
```

---

## 3. Example of `extends`

```java
class Animal {
    void sound() {
        System.out.println("Animal makes sound");
    }
}

class Dog extends Animal {
    void bark() {
        System.out.println("Dog barks");
    }
}

public class Main {
    public static void main(String[] args) {

        Dog d = new Dog();

        d.sound(); // inherited method
        d.bark();  // child method
    }
}
```

### Output

```text
Animal makes sound
Dog barks
```

---

## 4. `super` Keyword

`super` refers to the **parent class object**.

Used for:

1. Calling parent class variable
2. Calling parent class method
3. Calling parent class constructor

---

# A) `super` to Access Parent Variable

```java
class Animal {
    String color = "White";
}

class Dog extends Animal {
    String color = "Black";

    void printColor() {
        System.out.println(super.color); // parent variable
        System.out.println(color);       // child variable
    }
}

public class Main {
    public static void main(String[] args) {
        Dog d = new Dog();
        d.printColor();
    }
}
```

### Output

```text
White
Black
```

---

# B) `super` to Call Parent Method

```java
class Animal {
    void sound() {
        System.out.println("Animal sound");
    }
}

class Dog extends Animal {

    void sound() {
        System.out.println("Dog barks");
    }

    void display() {
        super.sound(); // parent method
        sound();       // child method
    }
}

public class Main {
    public static void main(String[] args) {
        Dog d = new Dog();
        d.display();
    }
}
```

### Output

```text
Animal sound
Dog barks
```

---

# C) `super()` to Call Parent Constructor

```java
class Animal {

    Animal() {
        System.out.println("Animal Constructor");
    }
}

class Dog extends Animal {

    Dog() {
        super(); // calls parent constructor
        System.out.println("Dog Constructor");
    }
}

public class Main {
    public static void main(String[] args) {
        Dog d = new Dog();
    }
}
```

### Output

```text
Animal Constructor
Dog Constructor
```

---

# Important Points

### `extends`

* Used for inheritance
* Java supports:

  * Single inheritance
  * Multilevel inheritance
  * Hierarchical inheritance

Java does NOT support multiple inheritance with classes.

---

### `super`

* Refers to immediate parent class
* Must be first statement in constructor
* Cannot be used in static methods directly

---
