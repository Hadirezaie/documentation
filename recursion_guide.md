# 🌀 Recursion

## 📖 Simple Definition

**Recursion** means:
- A function calls itself (self-referential).
- A large problem is broken down into smaller problems, and this continues until a **base case** is reached.

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
