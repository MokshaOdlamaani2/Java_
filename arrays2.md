
# 1️⃣ Print Array Elements

```java
public class PrintArray {
    public static void main(String[] args) {
        int[] arr = {10, 20, 30, 40};

        for (int i = 0; i < arr.length; i++) {
            System.out.println(arr[i]);
        }
    }
}
```

---

# 2️⃣ Sum of Elements

```java
public class SumArray {
    public static void main(String[] args) {
        int[] arr = {1, 2, 3, 4};
        int sum = 0;

        for (int num : arr) {
            sum += num;
        }

        System.out.println("Sum = " + sum);
    }
}
```

---

# 3️⃣ Largest Element

```java
public class LargestElement {
    public static void main(String[] args) {
        int[] arr = {5, 9, 2, 7};
        int max = arr[0];

        for (int i = 1; i < arr.length; i++) {
            if (arr[i] > max)
                max = arr[i];
        }

        System.out.println("Largest = " + max);
    }
}
```

---

# 4️⃣ Smallest Element

```java
public class SmallestElement {
    public static void main(String[] args) {
        int[] arr = {8, 3, 6, 1};
        int min = arr[0];

        for (int i = 1; i < arr.length; i++) {
            if (arr[i] < min)
                min = arr[i];
        }

        System.out.println("Smallest = " + min);
    }
}
```

---

# 5️⃣ Reverse Array

```java
public class ReverseArray {
    public static void main(String[] args) {
        int[] arr = {1, 2, 3, 4};

        for (int i = arr.length - 1; i >= 0; i--) {
            System.out.print(arr[i] + " ");
        }
    }
}
```

---

# 6️⃣ Array Palindrome

```java
public class ArrayPalindrome {
    public static void main(String[] args) {
        int[] arr = {1, 2, 3, 2, 1};
        boolean flag = true;

        for (int i = 0; i < arr.length / 2; i++) {
            if (arr[i] != arr[arr.length - 1 - i]) {
                flag = false;
                break;
            }
        }

        if (flag)
            System.out.println("Palindrome");
        else
            System.out.println("Not Palindrome");
    }
}
```

---

# 7️⃣ Search Element (Linear Search)

```java
public class LinearSearch {
    public static void main(String[] args) {
        int[] arr = {10, 20, 30, 40};
        int key = 30;
        boolean found = false;

        for (int num : arr) {
            if (num == key) {
                found = true;
                break;
            }
        }

        System.out.println(found ? "Found" : "Not Found");
    }
}
```

---

# 8️⃣ Count Even and Odd

```java
public class EvenOdd {
    public static void main(String[] args) {
        int[] arr = {1, 2, 3, 4, 5};
        int even = 0, odd = 0;

        for (int num : arr) {
            if (num % 2 == 0)
                even++;
            else
                odd++;
        }

        System.out.println("Even = " + even);
        System.out.println("Odd = " + odd);
    }
}
```

---

# 9️⃣ Copy Array

```java
public class CopyArray {
    public static void main(String[] args) {
        int[] arr1 = {1, 2, 3};
        int[] arr2 = new int[arr1.length];

        for (int i = 0; i < arr1.length; i++) {
            arr2[i] = arr1[i];
        }

        for (int num : arr2) {
            System.out.print(num + " ");
        }
    }
}
```

---

# 🔟 Second Largest Element

```java
public class SecondLargest {
    public static void main(String[] args) {
        int[] arr = {10, 20, 5, 15};
        int largest = arr[0];
        int second = arr[0];

        for (int i = 1; i < arr.length; i++) {
            if (arr[i] > largest) {
                second = largest;
                largest = arr[i];
            } else if (arr[i] > second && arr[i] != largest) {
                second = arr[i];
            }
        }

        System.out.println("Second Largest = " + second);
    }
}
```

---

# 1️⃣1️⃣ Remove Duplicates

```java
public class RemoveDuplicates {
    public static void main(String[] args) {
        int[] arr = {1, 2, 2, 3, 4, 4};

        for (int i = 0; i < arr.length; i++) {
            boolean duplicate = false;

            for (int j = 0; j < i; j++) {
                if (arr[i] == arr[j]) {
                    duplicate = true;
                    break;
                }
            }

            if (!duplicate)
                System.out.print(arr[i] + " ");
        }
    }
}
```

---

# 1️⃣2️⃣ Frequency of Elements

```java
public class Frequency {
    public static void main(String[] args) {
        int[] arr = {1, 2, 2, 3, 1};

        for (int i = 0; i < arr.length; i++) {
            int count = 1;
            boolean visited = false;

            for (int k = 0; k < i; k++) {
                if (arr[i] == arr[k]) {
                    visited = true;
                    break;
                }
            }

            if (visited)
                continue;

            for (int j = i + 1; j < arr.length; j++) {
                if (arr[i] == arr[j])
                    count++;
            }

            System.out.println(arr[i] + " occurs " + count + " times");
        }
    }
}
```

---

# 1️⃣3️⃣ Sort Array (Bubble Sort)

```java
public class BubbleSort {
    public static void main(String[] args) {
        int[] arr = {5, 3, 8, 1};

        for (int i = 0; i < arr.length - 1; i++) {
            for (int j = 0; j < arr.length - 1 - i; j++) {
                if (arr[j] > arr[j + 1]) {
                    int temp = arr[j];
                    arr[j] = arr[j + 1];
                    arr[j + 1] = temp;
                }
            }
        }

        for (int num : arr)
            System.out.print(num + " ");
    }
}
```

---

# 1️⃣4️⃣ Check if Two Arrays are Equal

```java
public class ArrayEqual {
    public static void main(String[] args) {
        int[] arr1 = {1, 2, 3};
        int[] arr2 = {1, 2, 3};

        boolean equal = true;

        if (arr1.length != arr2.length)
            equal = false;
        else {
            for (int i = 0; i < arr1.length; i++) {
                if (arr1[i] != arr2[i]) {
                    equal = false;
                    break;
                }
            }
        }

        System.out.println(equal ? "Equal" : "Not Equal");
    }
}
```

---

# 1️⃣5️⃣ Merge Two Arrays

```java
public class MergeArrays {
    public static void main(String[] args) {
        int[] arr1 = {1, 2, 3};
        int[] arr2 = {4, 5, 6};

        int[] merged = new int[arr1.length + arr2.length];

        for (int i = 0; i < arr1.length; i++)
            merged[i] = arr1[i];

        for (int i = 0; i < arr2.length; i++)
            merged[arr1.length + i] = arr2[i];

        for (int num : merged)
            System.out.print(num + " ");
    }
}
```

---


