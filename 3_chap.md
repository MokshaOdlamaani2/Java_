 Basic Java Programs

### 1. Print Personal Details

java

```java
class Main {
    public static void main(String[] args) {
        String name = "Rahul";
        int age = 22;
        String city = "Hyderabad";

        System.out.println("Name: " + name);
        System.out.println("Age: " + age);
        System.out.println("City: " + city);
    }
}
```

Important logic: Use variables to store personal details and `println()` to display them.

### 2. Calculate Total and Average Marks

java

```java
class Main {
    public static void main(String[] args) {
        int m1 = 80, m2 = 90, m3 = 70;

        int total = m1 + m2 + m3;
        double avg = total / 3.0;

        System.out.println("Total: " + total);
        System.out.println("Average: " + avg);
    }
}
```

Important logic: Total is the addition of marks, and average is total divided by the number of subjects.

### 3. Simple Calculator

java

```java
class Main {
    public static void main(String[] args) {
        int a = 20, b = 10;
        char op = '+';

        switch (op) {
            case '+':
                System.out.println(a + b);
                break;
            case '-':
                System.out.println(a - b);
                break;
            case '*':
                System.out.println(a * b);
                break;
            case '/':
                System.out.println(a / b);
                break;
            default:
                System.out.println("Invalid");
        }
    }
}
```

Important logic: Use `switch` to perform calculations based on the selected operator.

### 4. Swap Two Numbers

java

```java
class Main {
    public static void main(String[] args) {
        int a = 10, b = 20;

        int temp = a;
        a = b;
        b = temp;

        System.out.println(a);
        System.out.println(b);
    }
}
```

Important logic: Use a temporary variable to store one number while exchanging their values.

### 5. Celsius to Fahrenheit

java

```java
class Main {
    public static void main(String[] args) {
        double c = 37;

        double f = (c * 9 / 5) + 32;

        System.out.println(f);
    }
}
```

Important logic: Fahrenheit = (Celsius × 9/5) + 32.

# Day 2 – Conditional Statements

### 1. Even or Odd

java

```java
class Main {
    public static void main(String[] args) {
        int num = 10;

        if (num % 2 == 0) {
            System.out.println("Even");
        } else {
            System.out.println("Odd");
        }
    }
}
```

Important logic: Use `% 2` to check whether the remainder is zero or not.

### 2. Positive, Negative or Zero

java

```java
class Main {
    public static void main(String[] args) {
        int num = -5;

        if (num > 0) {
            System.out.println("Positive");
        } else if (num < 0) {
            System.out.println("Negative");
        } else {
            System.out.println("Zero");
        }
    }
}
```

Important logic: Compare the number with zero using `if-else if`.

### 3. Largest of Three Numbers

java

```java
class Main {
    public static void main(String[] args) {
        int a = 10, b = 25, c = 15;

        if (a >= b && a >= c) {
            System.out.println(a);
        } else if (b >= a && b >= c) {
            System.out.println(b);
        } else {
            System.out.println(c);
        }
    }
}
```

Important logic: Use `&&` to check whether one number is greater than or equal to both other numbers.

### 4. Leap Year Checker

java

```java
class Main {
    public static void main(String[] args) {
        int year = 2024;

        if (year % 400 == 0) {
            System.out.println("Leap Year");
        } else if (year % 100 == 0) {
            System.out.println("Not Leap Year");
        } else if (year % 4 == 0) {
            System.out.println("Leap Year");
        } else {
            System.out.println("Not Leap Year");
        }
    }
}
```

Important logic: A year divisible by 400 or divisible by 4 but not 100 is a leap year.

### 5. Grade Calculator

java

```java
class Main {
    public static void main(String[] args) {
        int marks = 85;

        if (marks >= 90) {
            System.out.println("A Grade");
        } else if (marks >= 80) {
            System.out.println("B Grade");
        } else if (marks >= 70) {
            System.out.println("C Grade");
        } else if (marks >= 50) {
            System.out.println("D Grade");
        } else {
            System.out.println("Fail");
        }
    }
}
```

Important logic: Use `if-else if` to check marks from highest range to lowest.

# Day 3 – Looping Programs

### 1. Multiplication Table

java

```java
class Main {
    public static void main(String[] args) {
        int num = 5;

        for (int i = 1; i <= 10; i++) {
            System.out.println(num + " x " + i + " = " + (num * i));
        }
    }
}
```

Important logic: Multiply the given number by each loop value from 1 to 10.

### 2. Sum of First N Numbers

java

```java
class Main {
    public static void main(String[] args) {
        int n = 10;
        int sum = 0;

        for (int i = 1; i <= n; i++) {
            sum = sum + i;
        }

        System.out.println(sum);
    }
}
```

Important logic: Add every loop value to `sum` until N is reached.

### 3. Factorial

java

```java
class Main {
    public static void main(String[] args) {
        int num = 5;
        int fact = 1;

        for (int i = 1; i <= num; i++) {
            fact = fact * i;
        }

        System.out.println(fact);
    }
}
```

Important logic: Multiply all numbers from 1 to the given number, starting with `fact = 1`.

### 4. Count Digits

java

```java
class Main {
    public static void main(String[] args) {
        int num = 12345;
        int count = 0;

        num = Math.abs(num);

        if (num == 0) {
            count = 1;
        } else {
            while (num != 0) {
                count++;
                num = num / 10;
            }
        }

        System.out.println(count);
    }
}
```

Important logic: Divide the number by 10 repeatedly and increase count in each iteration.

### 5. Reverse a Number

java

```java
class Main {
    public static void main(String[] args) {
        int num = 1234;
        int temp = num;
        int rev = 0;

        while (temp != 0) {
            int digit = temp % 10;
            rev = rev * 10 + digit;
            temp = temp / 10;
        }

        System.out.println(rev);
    }
}
```

Important logic: Extract the last digit using `% 10`, add it to reverse after multiplying reverse by 10, and remove the digit using `/ 10`.

# Day 4 – Number Logic Programs

### 1. Palindrome Number

java

```java
class Main {
    public static void main(String[] args) {
        int num = 121;
        int temp = num;
        int rev = 0;

        while (temp != 0) {
            int digit = temp % 10;
            rev = rev * 10 + digit;
            temp = temp / 10;
        }

        if (num == rev) {
            System.out.println("Palindrome");
        } else {
            System.out.println("Not Palindrome");
        }
    }
}
```

Important logic: Reverse the number and compare it with the original number.

### 2. Armstrong Number

java

```java
class Main {
    public static void main(String[] args) {
        int num = 153;
        int temp = num;
        int count = 0;
        int sum = 0;

        int n = num;

        while (n != 0) {
            count++;
            n = n / 10;
        }

        if (num == 0) {
            count = 1;
        }

        while (temp != 0) {
            int digit = temp % 10;
            sum = sum + (int) Math.pow(digit, count);
            temp = temp / 10;
        }

        if (num == sum) {
            System.out.println("Armstrong");
        } else {
            System.out.println("Not Armstrong");
        }
    }
}
```

Important logic: Add each digit raised to the power of the total digit count and compare the sum with the original number.

### 3. Prime Number

java

```java
class Main {
    public static void main(String[] args) {
        int num = 17;
        int count = 0;

        if (num <= 1) {
            count++;
        } else {
            for (int i = 2; i <= num / i; i++) {
                if (num % i == 0) {
                    count++;
                    break;
                }
            }
        }

        if (count == 0) {
            System.out.println("Prime");
        } else {
            System.out.println("Not Prime");
        }
    }
}
```

Important logic: If any number from 2 to the square root divides the given number, it is not prime.

### 4. Print Prime Numbers in a Range

java

```java
class Main {
    public static void main(String[] args) {
        int start = 1;
        int end = 50;

        for (int i = start; i <= end; i++) {
            int count = 0;

            if (i <= 1) {
                continue;
            }

            for (int j = 2; j <= i / j; j++) {
                if (i % j == 0) {
                    count++;
                    break;
                }
            }

            if (count == 0) {
                System.out.print(i + " ");
            }
        }
    }
}
```

Important logic: Use a nested loop to check each number's divisibility and print only numbers with no divisors.

### 5\. Fibonacci Series

java

```java
class Main {
    public static void main(String[] args) {
        int a = 0;
        int b = 1;
        int c;

        for (int i = 1; i <= 9; i++) {
            System.out.print(a + " ");

            c = a + b;
            a = b;
            b = c;
        }
    }
}
```

## 1. Sum of digits

Example: 122 → 1 + 2 + 2 = 5

java

```java

class Main {
    public static void main(String[] args) {
        int num = 122;
        int sums = 0;

        while (num != 0) {
            int digits = num % 10;
            sums = sums + digits;
            num = num / 10;
        }

        System.out.println("Sum of digits: " + sums);
    }
}
```

Output:

text

```text
Sum of digits: 5
```

## 2. GCD of two numbers

GCD means the greatest common divisor of two numbers.

Example: 12 and 18 → GCD = 6

java

```java

class Main {
    public static void main(String[] args) {
        int a = 12;
        int b = 18;
        int gcd = 1;

        int i = 1;

        while (i <= a && i <= b) {
            if (a % i == 0 && b % i == 0) {
                gcd = i;
            }
            i++;
        }

        System.out.println("GCD: " + gcd);
    }
}
```

Output:

text

```text
GCD: 6
```

## 3. LCM of two numbers

LCM means the least common multiple of two numbers.

Example: 12 and 18 → LCM = 36

java

```java

class Main {
    public static void main(String[] args) {
        int a = 12;
        int b = 18;

        int lcm = (a > b) ? a : b;

        while (true) {
            if (lcm % a == 0 && lcm % b == 0) {
                break;
            }
            lcm++;
        }

        System.out.println("LCM: " + lcm);
    }
}
```

Output:

text

```text
LCM: 36
```

Learn more

## 4. Perfect number

A perfect number is a number whose sum of proper divisors equals the number itself.

Example: 6 → 1 + 2 + 3 = 6

java

```java

class Main {
    public static void main(String[] args) {
        int num = 6;
        int sum = 0;
        int i = 1;

        while (i < num) {
            if (num % i == 0) {
                sum = sum + i;
            }
            i++;
        }

        if (sum == num) {
            System.out.println("Perfect number");
        } else {
            System.out.println("Not a perfect number");
        }
    }
}
```

Output:

text

```text
Perfect number
```

## 5. Find all divisors of a number

Example: 12 → 1, 2, 3, 4, 6, 12

java

```java

class Main {
    public static void main(String[] args) {
        int num = 12;
        int i = 1;

        System.out.println("Divisors are:");

        while (i <= num) {
            if (num % i == 0) {
                System.out.println(i);
            }
            i++;
        }
    }
}
```

Output:

text

```text
Divisors are:
1
2
3
4
6
12


## 1. First understand nested loops

A nested loop means one `for` loop inside another `for` loop.

java

```java
for (int i = 1; i <= 3; i++) {

    for (int j = 1; j <= 4; j++) {
        System.out.print("* ");
    }

    System.out.println();
}
```

Output:

text

```text
* * * *
* * * *
* * * *
```

Understand the two loops:

- Outer loop (`i`) controls the number of rows.
- Inner loop (`j`) controls the number of columns (stars).
- `System.out.print()` prints on the same line.
- `System.out.println()` moves to the next line.

Remember this simple rule

Outer loopNumber of rows

Inner loopNumber of columns

# 2. Different star patterns

## Pattern 1: Right-angle star triangle

Output:

text

```text
*
* *
* * *
* * * *
* * * * *
```

Logic:

- Row 1 → 1 star
- Row 2 → 2 stars
- Row 3 → 3 stars
- Row 4 → 4 stars
- Row 5 → 5 stars

The number of stars is equal to the row number (`i`).

Java code:

java

```java
public class Main {
    public static void main(String[] args) {

        for (int i = 1; i <= 5; i++) {

            for (int j = 1; j <= i; j++) {
                System.out.print("* ");
            }

            System.out.println();
        }
    }
}
```

Important logic: `j <= i`

This means the inner loop runs as many times as the current row number.

## Pattern 2: Inverted star triangle

Output:

text

```text
* * * * *
* * * *
* * *
* *
*
```

Logic:

- Row 1 → 5 stars
- Row 2 → 4 stars
- Row 3 → 3 stars
- Row 4 → 2 stars
- Row 5 → 1 star

Java code:

java

```java
for (int i = 5; i >= 1; i--) {

    for (int j = 1; j <= i; j++) {
        System.out.print("* ");
    }

    System.out.println();
}
```

Notice the difference: the outer loop decreases from 5 to 1.

# 3. Number triangle

Output:

text

```text
1
1 2
1 2 3
1 2 3 4
1 2 3 4 5
```

Logic:

Here, instead of printing `*`, we print the value of `j`.

Java code:

java

```java
public class Main {
    public static void main(String[] args) {

        for (int i = 1; i <= 5; i++) {

            for (int j = 1; j <= i; j++) {
                System.out.print(j + " ");
            }

            System.out.println();
        }
    }
}
```

The key change is:

java

```java
System.out.print(j + " ");
```

Earlier, we printed `"* "`. Now we print `j`.

# 4. Pyramid pattern

Output:

text

```text
        *
      * *
    * * *
  * * * *
* * * * *
```

Logic:

A pyramid needs two things:

1. Spaces before the stars.
2. Stars after the spaces.

For 5 rows:

| Row | Spaces | Stars |
| --- | --- | --- |
| 1 | 4 | 1 |
| 2 | 3 | 2 |
| 3 | 2 | 3 |
| 4 | 1 | 4 |
| 5 | 0 | 5 |

Java code:

java

```java
public class Main {
    public static void main(String[] args) {

        for (int i = 1; i <= 5; i++) {

            // Print spaces
            for (int j = 1; j <= 5 - i; j++) {
                System.out.print("  ");
            }

            // Print stars
            for (int j = 1; j <= i; j++) {
                System.out.print("* ");
            }

            System.out.println();
        }
    }
}
```

Remember:

- Spaces = `n - i`
- Stars = `i`

Where `n` is the total number of rows.

# 5. Floyd's triangle

Output:

text

```text
1
2 3
4 5 6
7 8 9 10
11 12 13 14 15
```

Logic:

Here, we need one extra variable called `num`.

- First row prints 1 number.
- Second row prints 2 numbers.
- Third row prints 3 numbers.
- Numbers continue increasing without restarting.

Java code:

java

```java
public class Main {
    public static void main(String[] args) {

        int num = 1;

        for (int i = 1; i <= 5; i++) {

            for (int j = 1; j <= i; j++) {

                System.out.print(num + " ");
                num++;
            }

            System.out.println();
        }
    }
}
```

Understand these two statements:

java

```java
System.out.print(num + " ");
num++;
```

- First statement prints the current number.
- Second statement increases the number by 1.

For example:

| Row | Numbers printed |
| --- | --- |
| 1 | 1 |
| 2 | 2, 3 |
| 3 | 4, 5, 6 |
| 4 | 7, 8, 9, 10 |

# 6. Hollow square pattern

Output:

text

```text
* * * * *
*       *
*       *
*       *
* * * * *
```

This pattern is slightly different because we print stars only on the boundaries.

Logic:

We need to check four conditions:

- First row → print stars.
- Last row → print stars.
- First column → print stars.
- Last column → print stars.
- Otherwise → print spaces.

Java code:

java

```java
public class Main {
    public static void main(String[] args) {

        int n = 5;

        for (int i = 1; i <= n; i++) {

            for (int j = 1; j <= n; j++) {

                if (i == 1 || i == n ||
                    j == 1 || j == n) {

                    System.out.print("* ");
                } else {
                    System.out.print("  ");
                }
            }

            System.out.println();
        }
    }
}
```

Most important condition:

java

```java
if (i == 1 || i == n || j == 1 || j == n)
```

Here:

- `i == 1` → first row.
- `i == n` → last row.
- `j == 1` → first column.
- `j == n` → last column.
- `||` means OR.

