

## What is a String?

A **String** is a sequence of characters (text).

Examples:

```java
"Hello"
"Java"
"123"
```

In Java, `String` is a **class**, not a primitive data type.

---

## Creating Strings

### 1. Using string literal (most common)

```java
String name = "Alice";
```

### 2. Using `new` keyword

```java
String name = new String("Alice");
```

👉 Prefer **string literals**. They are memory-efficient.

---

## Printing a String

```java
String msg = "Welcome to Java";
System.out.println(msg);
```

---

## String Concatenation (joining strings)

### Using `+`

```java
String first = "Hello";
String last = "World";

System.out.println(first + " " + last);
```

### With numbers

```java
int age = 20;
System.out.println("Age: " + age);
```

⚠️ Order matters:

```java
System.out.println(10 + 20 + " Java"); // 30 Java
System.out.println("Java " + 10 + 20); // Java 1020
```

---

## Common String Methods

```java
String text = "Java Programming";
```

| Method           | Description          | Example                 |
| ---------------- | -------------------- | ----------------------- |
| `length()`       | Number of characters | `text.length()`         |
| `toUpperCase()`  | Uppercase            | `text.toUpperCase()`    |
| `toLowerCase()`  | Lowercase            | `text.toLowerCase()`    |
| `charAt(i)`      | Character at index   | `text.charAt(0)`        |
| `substring(a,b)` | Part of string       | `text.substring(0,4)`   |
| `contains()`     | Check text           | `text.contains("Java")` |
| `equals()`       | Compare content      | `text.equals("Java")`   |

Example:

```java
System.out.println(text.length());     // 16
System.out.println(text.charAt(0));    // J
```

---

## Comparing Strings (VERY IMPORTANT)

❌ Wrong:

```java
if (s1 == s2)
```

✅ Correct:

```java
if (s1.equals(s2))
```

Why?
`==` compares **memory location**, `equals()` compares **content**.

---

## String is Immutable

Once created, a string **cannot be changed**.

```java
String s = "Java";
s.concat(" Language");

System.out.println(s); // Java
```

To change:

```java
s = s.concat(" Language");
```

---

## `StringBuilder` (for modifications)

Used when you change strings often.

```java
StringBuilder sb = new StringBuilder("Hello");
sb.append(" Java");

System.out.println(sb); // Hello Java
```

---

## Taking String input (User input)

```java
import java.util.Scanner;

Scanner sc = new Scanner(System.in);
String name = sc.nextLine();

System.out.println("Hello " + name);
```

---

## Common beginner mistakes 🚫

* Using `==` instead of `equals()`
* Forgetting strings start at index `0`
* Trying to modify strings directly
* Confusing `length()` with array length
**practice with solutions** 

## 1. Reverse a String

### Problem

Input: `"Java"`
Output: `"avaJ"`

### Solution (using loop)

```java
public class ReverseString {
    public static void main(String[] args) {
        String s = "Java";
        String rev = "";

        for (int i = s.length() - 1; i >= 0; i--) {
            rev = rev + s.charAt(i);
        }

        System.out.println("Reversed: " + rev);
    }
}
```

---

## 2. Check Palindrome

A string that reads the same forward and backward.

### Example

Input: `"madam"`
Output: `Palindrome`

```java
public class Palindrome {
    public static void main(String[] args) {
        String s = "madam";
        String rev = "";

        for (int i = s.length() - 1; i >= 0; i--) {
            rev += s.charAt(i);
        }

        if (s.equals(rev)) {
            System.out.println("Palindrome");
        } else {
            System.out.println("Not Palindrome");
        }
    }
}
```

---

## 3. Count Vowels in a String

### Input

`"Java Programming"`

### Output

Number of vowels

```java
public class CountVowels {
    public static void main(String[] args) {
        String s = "Java Programming".toLowerCase();
        int count = 0;

        for (int i = 0; i < s.length(); i++) {
            char ch = s.charAt(i);
            if (ch == 'a' || ch == 'e' || ch == 'i' || ch == 'o' || ch == 'u') {
                count++;
            }
        }

        System.out.println("Vowels: " + count);
    }
}
```

---

## 4. Count Words in a Sentence

### Input

`"Java is easy to learn"`

```java
public class WordCount {
    public static void main(String[] args) {
        String s = "Java is easy to learn";

        String[] words = s.split(" ");
        System.out.println("Words count: " + words.length);
    }
}
```

---

## 5. Remove Spaces from a String

### Input

`"Java Programming"`

### Output

`"JavaProgramming"`

```java
public class RemoveSpaces {
    public static void main(String[] args) {
        String s = "Java Programming";

        s = s.replace(" ", "");
        System.out.println(s);
    }
}
```

---

## 6. Find Duplicate Characters

### Input

`"programming"`

```java
public class DuplicateCharacters {
    public static void main(String[] args) {
        String s = "programming";

        for (int i = 0; i < s.length(); i++) {
            for (int j = i + 1; j < s.length(); j++) {
                if (s.charAt(i) == s.charAt(j)) {
                    System.out.println("Duplicate: " + s.charAt(i));
                    break;
                }
            }
        }
    }
}
```

---

## 7. Convert Each Word’s First Letter to Uppercase

### Input

`"java is fun"`

### Output

`"Java Is Fun"`

```java
public class CapitalizeWords {
    public static void main(String[] args) {
        String s = "java is fun";
        String[] words = s.split(" ");
        String result = "";

        for (String word : words) {
            result += word.substring(0, 1).toUpperCase()
                    + word.substring(1) + " ";
        }

        System.out.println(result.trim());
    }
}
```

---

## 8. Count Characters (excluding spaces)

```java
public class CharacterCount {
    public static void main(String[] args) {
        String s = "Java Programming";
        int count = 0;

        for (int i = 0; i < s.length(); i++) {
            if (s.charAt(i) != ' ') {
                count++;
            }
        }

        System.out.println("Characters: " + count);
    }
}
```

---

