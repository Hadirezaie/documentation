# 🌀 Recursion

## 📖 Simple Definition

**Recursion** means:
- A function calls itself (self-referential).
- We break a large problem into smaller problems and continue this process until we reach a stopping condition (Base Case).

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
