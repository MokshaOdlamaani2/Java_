-

## 1️⃣ Method to **create an array**

```java
static int[] createArray() {
    int[] arr = {10, 20, 30, 40};
    return arr;
}
```

Usage:

```java
int[] myArray = createArray();
```

---

## 2️⃣ Method to **print an array**

```java
static void printArray(int[] arr) {
    for (int i = 0; i < arr.length; i++) {
        System.out.print(arr[i] + " ");
    }
    System.out.println();
}
```

Usage:

```java
printArray(myArray);
```

---

## 3️⃣ Method to **update an element**

```java
static void updateElement(int[] arr, int index, int value) {
    arr[index] = value;
}
```

Usage:

```java
updateElement(myArray, 1, 99);
printArray(myArray);
```

---

## 4️⃣ Method to **insert an element** (new array)

⚠️ Arrays are fixed size → we create a **new array**

```java
static int[] insertElement(int[] arr, int value) {
    int[] newArr = new int[arr.length + 1];

    for (int i = 0; i < arr.length; i++) {
        newArr[i] = arr[i];
    }

    newArr[arr.length] = value;
    return newArr;
}
```

Usage:

```java
myArray = insertElement(myArray, 50);
```

---

## 5️⃣ Method to **delete an element**

```java
static int[] deleteElement(int[] arr, int index) {
    int[] newArr = new int[arr.length - 1];
    int j = 0;

    for (int i = 0; i < arr.length; i++) {
        if (i != index) {
            newArr[j++] = arr[i];
        }
    }
    return newArr;
}
```

Usage:

```java
myArray = deleteElement(myArray, 2);
```

---

## 6️⃣ Method to **search an element**

```java
static int search(int[] arr, int key) {
    for (int i = 0; i < arr.length; i++) {
        if (arr[i] == key) {
            return i;
        }
    }
    return -1;
}
```

Usage:

```java
int index = search(myArray, 30);
```

---

## 7️⃣ Method to **find sum**

```java
static int sum(int[] arr) {
    int total = 0;
    for (int i = 0; i < arr.length; i++) {
        total += arr[i];
    }
    return total;
}
```

---

## 8️⃣ Method to **find maximum**

```java
static int max(int[] arr) {
    int max = arr[0];
    for (int i = 1; i < arr.length; i++) {
        if (arr[i] > max) {
            max = arr[i];
        }
    }
    return max;
}
```

---

## 9️⃣ Method to **reverse an array**

```java
static void reverse(int[] arr) {
    int start = 0;
    int end = arr.length - 1;

    while (start < end) {
        int temp = arr[start];
        arr[start] = arr[end];
        arr[end] = temp;

        start++;
        end--;
    }
}
```

---

## 🔟 Method to **sort an array** (basic)

```java
static void sort(int[] arr) {
    for (int i = 0; i < arr.length - 1; i++) {
        for (int j = i + 1; j < arr.length; j++) {
            if (arr[i] > arr[j]) {
                int temp = arr[i];
                arr[i] = arr[j];
                arr[j] = temp;
            }
        }
    }
}
```

---

## 1️⃣1️⃣ Full program example (REAL USE)

```java
public class Main {

    static void printArray(int[] arr) {
        for (int x : arr) {
            System.out.print(x + " ");
        }
        System.out.println();
    }

    public static void main(String[] args) {

        int[] arr = {10, 20, 30};

        printArray(arr);

        arr = insertElement(arr, 40);
        printArray(arr);

        reverse(arr);
        printArray(arr);
    }
}

