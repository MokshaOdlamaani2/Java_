

# 1. Keywords

## What is a Keyword?

A **keyword** is a word that has a special meaning in Java.

Java has reserved these words for specific purposes.

For example:

```java
class Student {
    
}
```

Here:

```text
class
```

is a keyword.

It tells Java that we are defining a class.

---

## Examples of Java Keywords

Some commonly used keywords are:

```text
class
public
private
protected
static
void
int
double
float
char
boolean
if
else
for
while
do
switch
case
break
continue
return
new
this
extends
implements
final
try
catch
finally
throw
throws
```

---

# 2. Important Keyword Examples

## `class`

Used to define a class.

```java
class Student {
}
```

---

## `public`

Specifies that something can be accessed from outside its class/package depending on the context.

Example:

```java
public class Student {
}
```

---

## `private`

Restricts access to the class where it is declared.

Example:

```java
private int age;
```

---

## `static`

Makes a member belong to the class rather than to individual objects.

Example:

```java
static int count;
```

---

## `void`

Indicates that a method does not return a value.

```java
void display() {
}
```

---

## `int`

Used to declare an integer variable.

```java
int age = 25;
```

---

## `new`

Used to create an object.

```java
Student s = new Student();
```

---

## `if`

Used for decision making.

```java
if (age >= 18) {
    System.out.println("Adult");
}
```

---

## `else`

Used when the `if` condition is false.

```java
if (age >= 18) {
    System.out.println("Adult");
} else {
    System.out.println("Minor");
}
```

---

## `return`

Used to return a value from a method or to return control from a method.

Example:

```java
return age;
```

---

# 3. Important Rules About Keywords

### Rule 1: Keywords cannot be used as identifiers

You cannot write:

```java
int class = 10;
```

This is invalid because `class` is a keyword.

---

### Rule 2: Keywords have predefined meanings

For example:

```java
int
```

already has a specific meaning in Java.

You cannot redefine its meaning.

---

### Rule 3: Java is case-sensitive

For example:

```text
class
```

is a keyword.

But:

```text
Class
```

is not the same word.

Java distinguishes uppercase and lowercase letters.

---

# 4. Variables

## What is a Variable?

A **variable** is a named memory location used to store data.

For example:

```java
int age = 25;
```

Here:

```text
int  → data type
age  → variable name
25   → value
```

Think of a variable as a **container** that stores a value.

```text
age
┌───────────┐
│    25     │
└───────────┘
```

---

# 5. Why Do We Need Variables?

Suppose you want to store a person's age.

You can write:

```java
int age = 25;
```

Now Java knows that:

* The variable is called `age`
* It stores an integer
* Its current value is `25`

You can use it later:

```java
System.out.println(age);
```

Output:

```text
25
```

---

# 6. Variable Declaration

Variable declaration means telling Java:

> I want to create a variable of a particular type.

Example:

```java
int age;
```

Here:

```text
int
```

is the data type.

```text
age
```

is the variable name.

At this point, we have declared the variable but haven't assigned a value to it.

---

# 7. Variable Initialization

Giving a value to a variable is called **initialization**.

Example:

```java
age = 25;
```

Now the variable contains:

```text
age → 25
```

---

# 8. Declaration and Initialization Together

You can do both at the same time:

```java
int age = 25;
```

This means:

```text
Declare age
      +
Assign 25
```

---

# 9. Changing a Variable's Value

A variable's value can usually be changed.

Example:

```java
int age = 25;

age = 26;
```

Initially:

```text
age → 25
```

After:

```text
age → 26
```

---

# 10. Examples of Variables

```java
int age = 25;
double salary = 45000.50;
char grade = 'A';
boolean passed = true;
String name = "John";
```

Here:

| Variable | Value      |
| -------- | ---------- |
| `age`    | `25`       |
| `salary` | `45000.50` |
| `grade`  | `'A'`      |
| `passed` | `true`     |
| `name`   | `"John"`   |

---

# 11. Types of Variables

Java variables can be classified into different categories.

The common categories are:

1. Local variables
2. Instance variables
3. Static/class variables

---

# 12. Local Variable

A variable declared inside a method, constructor, or block is generally a **local variable**.

Example:

```java
class Student {
    void display() {
        int age = 20;
        System.out.println(age);
    }
}
```

Here:

```text
age
```

is a local variable.

It is available within its applicable method/block.

---

# 13. Instance Variable

An instance variable is declared inside a class but outside methods, constructors, and blocks, and is associated with an object.

Example:

```java
class Student {
    int age;
    
    void display() {
        System.out.println(age);
    }
}
```

Here:

```text
age
```

is an instance variable.

Each object can have its own value.

---

# 14. Static Variable

A static variable belongs to the class rather than individual objects.

Example:

```java
class Student {
    static String college = "ABC College";
}
```

Here:

```text
college
```

is a static variable.

It is shared by the class's objects.

---

# 15. Identifiers

## What is an Identifier?

An **identifier** is the name given to a programming element.

Identifiers can be used for:

* Classes
* Variables
* Methods
* Objects
* Interfaces
* Packages

Examples:

```java
class Student {
    int age;

    void display() {
    }
}
```

Here:

```text
Student → class identifier
age     → variable identifier
display → method identifier
```

---

# 16. Identifier Rules

Java has rules for creating identifiers.

## Rule 1: Must begin with a letter, `_`, or `$`

Valid:

```text
name
_age
$salary
studentName
```

Invalid:

```text
1name
```

An identifier cannot normally start with a digit.

---

## Rule 2: Cannot contain spaces

Invalid:

```text
student name
```

Valid:

```text
studentName
```

---

## Rule 3: Cannot be a keyword

Invalid:

```java
int class;
```

because `class` is a keyword.

---

## Rule 4: Identifiers are case-sensitive

These are different identifiers:

```text
age
Age
AGE
```

Java treats them as different names.

---

## Rule 5: Special characters generally aren't allowed

For example:

```text
student-name
```

is not a valid identifier because `-` is not permitted as part of a normal Java identifier.

Use:

```text
studentName
```

instead.

---

# 17. Valid and Invalid Identifiers

| Identifier     | Valid? | Reason            |
| -------------- | ------ | ----------------- |
| `studentName`  | ✅      | Valid             |
| `age`          | ✅      | Valid             |
| `_age`         | ✅      | Valid             |
| `$salary`      | ✅      | Valid             |
| `student1`     | ✅      | Valid             |
| `1student`     | ❌      | Starts with digit |
| `student name` | ❌      | Contains space    |
| `class`        | ❌      | Keyword           |
| `student-name` | ❌      | Contains `-`      |

---

# 18. Identifier vs Variable

These terms are related but not exactly the same.

Consider:

```java
int age = 25;
```

Here:

```text
age
```

is an **identifier**.

It is specifically being used as the name of a **variable**.

So:

> Every variable has an identifier/name, but identifiers can name other things too, such as classes and methods.

Example:

```java
class Student {
    int age;

    void display() {
    }
}
```

```text
Student → identifier for class
age     → identifier for variable
display → identifier for method
```

---

# 19. Data Types

## What is a Data Type?

A **data type** tells Java:

> What kind of data a variable can store.

Example:

```java
int age = 25;
```

Here:

```text
int
```

tells Java that `age` stores an integer value.

---

# 20. Types of Data Types in Java

Java data types are broadly divided into:

```text
Data Types
│
├── Primitive
│
└── Non-Primitive / Reference
```

---

# 21. Primitive Data Types

Java has **8 primitive data types**:

```text
byte
short
int
long
float
double
char
boolean
```

These are fundamental built-in data types.

---

# 22. `byte`

`byte` is used for small integer values.

Size:

```text
8 bits
```

Range:

```text
-128 to 127
```

Example:

```java
byte age = 25;
```

---

# 23. `short`

`short` stores an integer value larger than `byte` but smaller than `int`.

Size:

```text
16 bits
```

Range:

```text
-32,768 to 32,767
```

Example:

```java
short salary = 30000;
```

---

# 24. `int`

`int` is commonly used for integer values.

Size:

```text
32 bits
```

Range:

```text
-2,147,483,648 to 2,147,483,647
```

Example:

```java
int age = 25;
```

For normal whole numbers, `int` is usually the default choice.

---

# 25. `long`

`long` is used for larger integer values.

Size:

```text
64 bits
```

Example:

```java
long population = 1400000000L;
```

The `L` indicates a long literal.

---

# 26. `float`

`float` is used to store decimal/floating-point values.

Size:

```text
32 bits
```

Example:

```java
float marks = 85.5f;
```

The `f` is used to indicate a float literal.

---

# 27. `double`

`double` is used for decimal values with greater precision than `float`.

Size:

```text
64 bits
```

Example:

```java
double salary = 45000.75;
```

For decimal calculations, `double` is commonly used unless there is a specific reason to use another type.

---

# 28. `char`

`char` stores a single character.

Size:

```text
16 bits
```

Example:

```java
char grade = 'A';
```

Notice that a character uses **single quotes**:

```text
'A'
```

Not:

```text
"A"
```

---

# 29. `boolean`

`boolean` stores a logical value.

It can have:

```text
true
false
```

Example:

```java
boolean passed = true;
```

Another example:

```java
boolean isStudent = false;
```

---

# 30. Primitive Data Type Summary

| Data Type |                            Size | Example             |
| --------- | ------------------------------: | ------------------- |
| `byte`    |                          8 bits | `byte x = 10;`      |
| `short`   |                         16 bits | `short x = 1000;`   |
| `int`     |                         32 bits | `int x = 100000;`   |
| `long`    |                         64 bits | `long x = 100000L;` |
| `float`   |                         32 bits | `float x = 10.5f;`  |
| `double`  |                         64 bits | `double x = 10.5;`  |
| `char`    |                         16 bits | `char x = 'A';`     |
| `boolean` | language-defined representation | `boolean x = true;` |

---

# 31. Non-Primitive / Reference Types

Examples include:

* String
* Arrays
* Classes
* Interfaces
* Enums

Example:

```java
String name = "Maria";
```

Here:

```text
String
```

is a reference type.

---

# 32. String

`String` is used to store a sequence of characters.

Example:

```java
String name = "Maria Jerome";
```

Output:

```text
Maria Jerome
```

A String uses **double quotes**:

```java
"Hello"
```

Compare:

```java
char grade = 'A';
String name = "Alex";
```

### Remember:

```text
char   → one character → 'A'
String → multiple characters → "Alex"
```

---

# 33. Primitive vs Reference Types

### Primitive

Stores a basic value directly.

Examples:

```java
int age = 25;
char grade = 'A';
boolean passed = true;
```

### Reference

A reference variable refers to an object.

Example:

```java
String name = "John";
```

Simple way to remember:

```text
Primitive
→ Basic built-in values

Reference
→ Refers to objects
```

---

# 34. Coding Standards

Coding standards are rules and guidelines that make code:

* Easy to read
* Easy to understand
* Easy to maintain
* Consistent
* Professional

---

# 35. Class Naming Convention

Class names generally use **PascalCase**.

Examples:

```text
Student
StudentDetails
AddressDetails
EmployeeManagement
```

Avoid:

```text
studentdetails
student_details
```

A class example:

```java
public class StudentDetails {
}
```

---

# 36. Variable Naming Convention

Variables generally use **camelCase**.

Examples:

```text
studentName
studentAge
employeeSalary
totalMarks
```

Example:

```java
int studentAge = 20;
String studentName = "John";
```

---

# 37. Method Naming Convention

Methods generally use **camelCase**.

Examples:

```text
displayDetails()
calculateSalary()
getStudentName()
setStudentName()
```

Example:

```java
void displayDetails() {
}
```

---

# 38. Constant Naming Convention

Constants are generally written in **UPPER_CASE**, with words separated by underscores.

Example:

```java
final int MAX_MARKS = 100;
```

Another:

```java
final double PI_VALUE = 3.14159;
```

---

# 39. Package Naming Convention

Package names are generally written in lowercase.

Example:

```text
com.company.project
```

or:

```text
com.example.student
```

---

# 40. Meaningful Names

Use names that clearly describe what a variable contains.

Good:

```java
int studentAge;
double monthlySalary;
String employeeName;
```

Poor:

```java
int x;
double a;
String s;
```

Meaningful names make programs easier to understand.

---

# 41. Complete Example

```java
public class StudentDetails {

    public static void main(String[] args) {

        String studentName = "Maria";
        int studentAge = 21;
        double marks = 85.5;
        char grade = 'A';
        boolean passed = true;

        System.out.println(studentName);
        System.out.println(studentAge);
        System.out.println(marks);
        System.out.println(grade);
        System.out.println(passed);
    }
}
```

Here:

```text
StudentDetails → Class identifier
studentName    → Variable identifier
String         → Data type
"Maria"        → String value

studentAge     → Variable identifier
int            → Data type
21             → Integer value

marks          → Variable identifier
double         → Data type
85.5           → Decimal value

grade          → Variable identifier
char           → Data type
'A'            → Character value

passed         → Variable identifier
boolean        → Data type
true           → Boolean value
```

---

# 42. Very Important Differences

## Keyword vs Identifier

### Keyword

A reserved word with a predefined meaning.

Example:

```text
class
int
public
static
```

### Identifier

A name given by the programmer.

Example:

```text
Student
studentName
displayDetails
```

---

## Variable vs Data Type

Example:

```java
int age = 20;
```

```text
int → Data type
age → Variable
20  → Value
```

---

## `char` vs `String`

```java
char grade = 'A';
String name = "Maria";
```

```text
char
→ Single character
→ Single quotes

String
→ Sequence of characters
→ Double quotes
```

---

# 43. Quick Revision

## Keywords

> Reserved words that have special meaning in Java.

Examples:

```text
class
public
static
void
int
if
else
return
new
```

---

## Variables

> Named storage locations used to store values.

Example:

```java
int age = 20;
```

---

## Identifiers

> Names given to programming elements such as classes, variables, and methods.

Examples:

```text
Student
studentAge
displayDetails
```

---

## Data Types

> Specify the type of data a variable can store.

Examples:

```text
int
double
char
boolean
String
```

---

# 44. Important Quiz Points

### Remember the 8 primitive data types:

```text
byte
short
int
long
float
double
char
boolean
```

### Remember:

```text
int → Whole numbers
long → Large whole numbers
float → Decimal
double → More precise decimal
char → Single character
boolean → true/false
```

### Remember:

```text
char → 'A'
String → "ABC"
```

### Identifier cannot:

* Start with a digit
* Contain spaces
* Be a Java keyword
* Normally contain special characters such as `-`

### Naming conventions:

```text
Class       → PascalCase
Variable    → camelCase
Method      → camelCase
Constant    → UPPER_CASE
Package     → lowercase
```

---

# 45. Final Memory Sheet

```text
KEYWORD
↓
Reserved Java word
Example: class, int, public

VARIABLE
↓
Stores a value
Example: int age = 20;

IDENTIFIER
↓
Name given to a programming element
Example: age, Student, displayDetails

DATA TYPE
↓
Defines what kind of data can be stored
Example: int, double, char, boolean
```

## Primitive Types

```text
byte
short
int
long
float
double
char
boolean
```

## Most Important Example

```java
int studentAge = 20;
```

```text
int
↓
Data Type

studentAge
↓
Identifier / Variable Name

20
↓
Value
```

## Most Important Rule

> **Keywords are predefined by Java, while identifiers are names created by the programmer.**
