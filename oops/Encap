## Encapsulation in Java (Practical Explanation)

**Encapsulation** means:

* Hiding the internal data of a class
* Allowing controlled access through methods

In practice:

* Variables are usually made `private`
* Access is provided using **getters** and **setters**

---

# 1. Why Encapsulation?

Without encapsulation:

```java
class Student {
    public int age;
}
```

Anyone can directly change `age`:

```java
Student s = new Student();
s.age = -100;   // invalid
```

This is unsafe.

---

# 2. Using Encapsulation Properly

```java
class Student {

    // private data members
    private String name;
    private int age;

    // getter methods
    public String getName() {
        return name;
    }

    public int getAge() {
        return age;
    }

    // setter methods
    public void setName(String n) {
        name = n;
    }

    public void setAge(int a) {

        // validation
        if(a > 0) {
            age = a;
        }
    }
}
```

---

# 3. Using the Class

```java
public class Main {

    public static void main(String[] args) {

        Student s = new Student();

        s.setName("Rahul");
        s.setAge(21);

        System.out.println(s.getName());
        System.out.println(s.getAge());
    }
}
```

### Output

```text
Rahul
21
```

---

# 4. Access Modifiers in Java

| Modifier    | Same Class | Same Package | Subclass | Other Package |
| ----------- | ---------- | ------------ | -------- | ------------- |
| `private`   | YES        | NO           | NO       | NO            |
| default     | YES        | YES          | NO       | NO            |
| `protected` | YES        | YES          | YES      | NO            |
| `public`    | YES        | YES          | YES      | YES           |

---

# 5. Practical Example with Validation

```java
class BankAccount {

    private double balance;

    public void deposit(double amount) {

        if(amount > 0) {
            balance += amount;
        }
    }

    public double getBalance() {
        return balance;
    }
}
```

Usage:

```java
BankAccount b = new BankAccount();

b.deposit(5000);

System.out.println(b.getBalance());
```

This prevents:

```java
b.balance = -100000; // NOT allowed
```

because `balance` is `private`.

---
