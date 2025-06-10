# 🌀 Recursion

## 📖 Simple Definition

**Recursion** means:

- A function calls itself (self-referential).
- We break a large problem into smaller problems and continue this process until we reach a stopping condition (**Base Case**).

---

## 📌 General Structure of a Recursive Function

```java
returnType functionName(parameters) {
    if (base case) {
        return result;
    } else {
        // do some processing
        return functionName(modified parameters); // recursive call
    }
}
```

✅ **Base Case (Stopping Condition)**  
If we don't have it, the function will call itself infinitely and eventually lead to a **StackOverflowError**.

---

## 📚 Important Applications of Recursion

| Application                     | Description                                                |
|--------------------------------|------------------------------------------------------------|
| Divide & Conquer Problems      | Like QuickSort, MergeSort, Binary Search                   |
| Recursive Data Structures      | Linked Lists, Trees, Graphs                                |
| Combinatorial Algorithms       | Generating all combinations, permutations, Tower of Hanoi  |
| Problems with Similar Subproblems | Fibonacci sequence, different paths in a matrix         |

---

## 🌟 Practical Examples in Java

### 🔰 Simple Example: Print Numbers from 1 to n

```java
public class RecursionExample {
    public static void printNumbers(int n) {
        if (n == 0) {
            return; // Base Case
        }
        printNumbers(n - 1); // Recursive Call
        System.out.println(n); // Process after recursive call
    }

    public static void main(String[] args) {
        printNumbers(5);
    }
}
```

**🔹 Output:**
```
1
2
3
4
5
```

⛔ If we don't have a stopping condition, the function will call infinitely.

---

### 🟡 Intermediate Example: Calculate Factorial (n!)

**Formula:**

- n! = n * (n - 1)!
- 0! = 1 (Base Case)

```java
public class FactorialExample {
    public static int factorial(int n) {
        if (n == 0) {
            return 1; // Base Case
        } else {
            return n * factorial(n - 1); // Recursive Call
        }
    }

    public static void main(String[] args) {
        System.out.println(factorial(5)); // 120
    }
}
```

**🔹 Output:**  
```
120
```

---

### 🟢 Advanced Example: Calculate nth Fibonacci Number

**Fibonacci Sequence:**  
0, 1, 1, 2, 3, 5, 8, 13, ...

**Formula:**

- fib(n) = fib(n - 1) + fib(n - 2)
- fib(0) = 0
- fib(1) = 1

```java
public class FibonacciExample {
    public static int fibonacci(int n) {
        if (n == 0) {
            return 0; // Base Case
        } else if (n == 1) {
            return 1; // Base Case
        } else {
            return fibonacci(n - 1) + fibonacci(n - 2); // Recursive Calls
        }
    }

    public static void main(String[] args) {
        System.out.println(fibonacci(7)); // 13
    }
}
```

**🔹 Output:**  
```
13
```

⚠️ **Important Note:** This method has slow execution time: **O(2ⁿ)**. For improvement, use **Memoization** or **Dynamic Programming**.

---

## 🎁 Other Real-World Applications of Recursion

- **File Processing**:  
  Recursively find all files in subdirectories.

- **Tree Structure**:  
  - Reading XML/JSON trees  
  - Traversing Binary Search Trees

- **Divide and Conquer Algorithms**:  
  - MergeSort  
  - QuickSort  
  - Binary Search

- **Solving Complex Puzzles**:  
  - Sudoku  
  - Tower of Hanoi

---

## ⚖️ Advantages and Disadvantages of Recursion

| Advantages                                     | Disadvantages                                  |
|-----------------------------------------------|------------------------------------------------|
| Shorter and more readable code                | High memory consumption (Stack)                |
| Simple solution for recursive problems        | Sometimes slower than iterative approach       |
| Suitable for recursive structures (trees, graphs) | Must define stopping condition correctly     |

---

## 💡 Golden Tips for Exams

✅ Always define a Base Case  
✅ Call the function with smaller input each time  
✅ Be able to visualize the Call Stack tree  
✅ Know both Recursive and Iterative versions of algorithms

---

## 🧪 Practice Problems (for Exam Preparation)

1️⃣ Calculate sum of numbers from 1 to n → `sum(n)`  
2️⃣ Calculate power of number aⁿ → `power(a, n)`  
3️⃣ Reverse a string → `reverse(String s)`  
4️⃣ Count number of ways to reach the end of n stairs → `stairs(n)`

---

## 🔚 Summary

👉 Recursion is a powerful tool but must be used carefully  
👉 Very useful in interviews and exams  
👉 Base case is very important  
👉 Call Stack must be well understood
