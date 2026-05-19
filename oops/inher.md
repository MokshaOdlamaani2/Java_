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


class Animal {

    String color = "White";

    Animal() {
        System.out.println("Animal Constructor Called");
    }

    void sound() {
        System.out.println("Animal makes sound");
    }
}

// extends keyword used here
class Dog extends Animal {

    String color = "Black";

    Dog() {

        // super() calls parent constructor
        super();

        System.out.println("Dog Constructor Called");
    }

    void display() {

        // super.color -> parent variable
        System.out.println("Parent Color: " + super.color);

        // child variable
        System.out.println("Child Color: " + color);

        // super.sound() -> parent method
        super.sound();
    }
}

class Main {

    public static void main(String[] args) {

        Dog d = new Dog();

        d.display();
    }
}
---


# 1. Inheritance

### Meaning

One class inherits another class.

```text id="r4u5ga"
Dog is an Animal
```

### Code

```java id="gvjlwm"
class Animal {

    void eat() {
        System.out.println("Animal eats");
    }
}

class Dog extends Animal {

    void bark() {
        System.out.println("Dog barks");
    }
}

class Main {
    public static void main(String[] args) {

        Dog d = new Dog();

        d.eat();
        d.bark();
    }
}
```

---

# 2. Inheritance + Association

### Meaning

* One class inherits another
* AND uses another class object

```text id="j1k4xp"
Dog is an Animal
Dog uses Collar
```

### Code

```java id="d0b8m7"
class Collar {

    String color = "Red";
}

class Animal {

    void eat() {
        System.out.println("Animal eats");
    }
}

class Dog extends Animal {

    Collar c = new Collar(); // Association

    void show() {
        System.out.println("Collar Color: " + c.color);
    }
}

class Main {

    public static void main(String[] args) {

        Dog d = new Dog();

        d.eat();
        d.show();
    }
}
```

---

# 3. Inheritance + Aggregation

### Meaning

* One class inherits another
* AND contains another independent object

```text id="x5qbcl"
Manager is an Employee
Manager has Department
```

### Code

```java id="jlwm1f"
class Department {

    String deptName;

    Department(String deptName) {
        this.deptName = deptName;
    }
}

class Employee {

    void work() {
        System.out.println("Employee works");
    }
}

class Manager extends Employee {

    Department d; // Aggregation

    Manager(Department d) {
        this.d = d;
    }

    void display() {
        System.out.println("Department: " + d.deptName);
    }
}

class Main {

    public static void main(String[] args) {

        Department d1 = new Department("IT");

        Manager m = new Manager(d1);

        m.work();
        m.display();
    }
}
```

✔ Department can exist independently.

---

# 4. Inheritance + Association + Aggregation

### Meaning

Uses all three together.

```text id="d9azjx"
Developer is an Employee
Developer uses Laptop
Developer has Department
```

---

### Code

```java id="9f8zrz"
class Laptop {

    String brand = "Dell";
}

class Department {

    String deptName;

    Department(String deptName) {
        this.deptName = deptName;
    }
}

class Employee {

    void work() {
        System.out.println("Employee working");
    }
}

class Developer extends Employee {

    Laptop l = new Laptop(); // Association

    Department d; // Aggregation

    Developer(Department d) {
        this.d = d;
    }

    void display() {

        System.out.println("Laptop: " + l.brand);

        System.out.println("Department: " + d.deptName);
    }
}

class Main {

    public static void main(String[] args) {

        Department d1 = new Department("Development");

        Developer dev = new Developer(d1);

        dev.work();

        dev.display();
    }
}
```

---

# Easy Understanding Table

| Concept     | Meaning |
| ----------- | ------- |
| Inheritance | IS-A    |
| Association | USES-A  |
| Aggregation | HAS-A   |

---

# Real-Life Combined Example

```text id="0r8cl7"
Developer IS-A Employee
Developer USES-A Laptop
Developer HAS-A Department
```

