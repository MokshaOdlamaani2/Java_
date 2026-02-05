
**Type casting** means converting one data type into another.

Example idea:

> Converting `int` to `double`, or `double` to `int`.

---

## Types of Type Casting in Java

There are **two main types**:

1. **Widening (Implicit) Casting**
2. **Narrowing (Explicit) Casting**

---

## 1. Widening Type Casting (Implicit)

✔ Happens **automatically**
✔ Converts **smaller → larger** data type
✔ No data loss

### Order:

```
byte → short → int → long → float → double
```

### Example:

```java
public class WideningCasting {
    public static void main(String[] args) {
        int a = 10;
        double b = a;   // automatic

        System.out.println(a);
        System.out.println(b);
    }
}
```

Output:

```
10
10.0
```

---

## 2. Narrowing Type Casting (Explicit)

⚠ Must be done **manually**
⚠ Converts **larger → smaller** data type
⚠ Data loss possible

### Example:

```java
public class NarrowingCasting {
    public static void main(String[] args) {
        double a = 10.75;
        int b = (int) a;  // explicit casting

        System.out.println(a);
        System.out.println(b);
    }
}
```

Output:

```
10.75
10
```

👉 Decimal part is **lost**, not rounded.

---

## 3. Type Casting with `char`

```java
public class CharCasting {
    public static void main(String[] args) {
        char ch = 'A';
        int ascii = ch;

        System.out.println(ascii); // 65
    }
}
```

### int to char

```java
int x = 66;
char ch = (char) x;

System.out.println(ch); // B
```

---

## 4. Type Casting in Expressions

```java
public class ExpressionCasting {
    public static void main(String[] args) {
        int a = 5, b = 2;

        double result = (double) a / b;
        System.out.println(result); // 2.5
    }
}
```

⚠ Without casting:

```java
5 / 2 = 2
```

---

## 5. String Type Casting (Conversion)

### String → int

```java
String s = "100";
int num = Integer.parseInt(s);
```

### int → String

```java
int n = 50;
String s = String.valueOf(n);
```

---

## 6. Boolean Type Casting

❌ **Not allowed**:

```java
int a = (int) true; // ERROR
```

✔ Use conditions instead.

---

## Common Beginner Mistakes 🚫

* Forgetting `(type)` in narrowing
* Expecting rounding instead of truncation
* Integer division errors
* Casting boolean values

---


Just say 😊
