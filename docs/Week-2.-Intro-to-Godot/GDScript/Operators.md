---
title: Operators and Computation
weight: 5
---

# Operators and Computation

Mathematics and logic are the two most essential ingredients of a code written in any programming language. Godot uses simple mathematical, comparison, and logical operators to perform calculations on variables. Let’s take a look at each of them.

#### Mathematical Operators

Mathematical operators are used for simple calculations between two or more variables.

| **Operator**       | **Symbol** | **Example**                  |
| ------------------ | ---------- | ---------------------------- |
| Addition           | +          | `var Sum = A + B`            |
| Subtraction        | -          | `var Difference = A - B`     |
| Multiplication     | \*         | `var Multiply = A * B`       |
| Division           | /          | `var Divide = A / B`         |
| Modulo (Remainder) | %          | `var Remainder = A % B`      |
| Square root        | sqrt       | `var Squareroot_A = sqrt(A)` |

#### Comparison and Logical Operators

| **Operator**             | **Symbol** | **Condition** | **Description**                                                   |
| ------------------------ | ---------- | ------------- | ----------------------------------------------------------------- |
| Equal To                 | ==         | `A == B`      | True if A is equal to B.                                          |
| Not Equal To             | !=         | `A ! = B`     | True if A is not equal to B.                                      |
| Less Than                | <          | `A < B`       | True if A is less than B.                                         |
| Greater Than             | >          | `A > B`       | True if A is greater than B.                                      |
| Less Than or Equal to    | <=         | `A < = B`     | True if A is either less than B OR equal to B.                    |
| Greater Than or Equal to | >=         | `A > = B`     | True if A is either greater than B OR equal to B.                 |
| And                      | &&         | `A && B`      | True if both A and B are true.                                    |
| Or                       | \|\|       | `A \|         | B`                                                                |
| Not                      | !          | `!A`          | If A is false, then return true. If A is true, then return false. |

#### SNIPPETS OF SYNTAX

**Mathematical Calculations Between Two Variables** `a` **and** `b`

```gdscript
var a = 50
var b = 20
var sum
var difference
var multiplication
var division
var remainder
var squareroot_a
var squareroot_b
func _ready():
      print("a = ", a)            # Printing the value of a
      print("b = ", b)            # Printing the value of b
      sum = a + b
      print("sum= ", sum)
      difference = a - b
      print("difference= ", difference)
      multiplication = a * b
      print("multiplication = ", multiplication)
      division = a / b            # a is divided by b
      print("division = ", division)
      remainder = a % b           # Remainder when a is divided by b
      print("remainder = ", remainder)
      squareroot_a = sqrt(a)
      print("squareroot of a= ", squareroot_a)
      squareroot_b = sqrt(b)
      print("squareroot of b= ", squareroot_b)
```

**Output**

```
a = 50
b = 20
sum = 70
difference = 30
multiplication = 1000
division = 2
remainder = 10
squareroot of a = 7.071068
squareroot of b = 4.472136
```
