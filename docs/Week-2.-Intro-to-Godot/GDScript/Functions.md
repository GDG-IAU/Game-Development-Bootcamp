---
title: Functions
weight: 2
---

# Functions

A function is an organized block of code that groups together related actions or tasks. It helps make the code more readable by avoiding writing the same code in multiple places. For example, you might have a function to calculate and display the total points a player earns in a game. Since these points will keep changing throughout the game, we can use this function every time we want to update the score.

The function `_ready()` is an important GDScript function that is called every time a node is created in the Scene tree. Another important function is called `_process (_delta)` , which is executed for every frame in the game. Here, `delta` represents the total time between each frame. These two built-in functions can be changed according to our programming needs. We can also create our own functions for different tasks, such as creating a coin-collection system, spawning enemies, and calculating player health.

Every function starts with the keyword `func` and can return a value that we can use somewhere else in our code. You can also choose to pass values, called arguments, to a function if you need to use them there.

In the first example given in the “Snippets of Syntax”, we declare a function for printing a user’s name. This function, called `print_my_name`, has an input parameter called `my_name`. We pass the string **"Lisa"** as an input to this function when we call it in the `_ready()` function . In this way, the variable `my_name` stores the string "Lisa", and the sentence **"Hi, my name is Lisa"** is printed at the output.

In the second example, we have a function called `add` that takes two numbers, `num1` and `num2`, as input, prints each of them, and returns their sum to the `_ready()` function. In `_ready()`, we declare a variable called `my_sum` and pass the values 5 and 6 to `num1` and `num2`, respectively. When we print the variable `my_sum`, the sum of these two numbers, i.e., 11, is displayed at the output.

### SNIPPETS OF SYNTAX

#### 1. Passing and Printing a Name

```gdscript
func print_my_name(my_name):
     print("Hi, my name is ",my_name)

func _ready():
     print_my_name("Lisa")
```

**Output**

`Hi, my name is Lisa`

#### 2. Passing Numbers to a Function and Adding Them Together

```gdscript
func add(num1, num2):
     print("num1 = ",num1)
     print("num2 = ",num2)
     return num1 + num2

func_ready():
     var my_sum = add(5, 6)
     print(my_sum)
```

**Output**

```
num1 = 5
num2 = 6
11
```

You can declare variables either **locally (inside a function)** or **globally (outside of any function)**. A local variable is visible only in the function in which it is declared, while a global variable is visible to all the functions in the code. In the example shown earlier, the variable `my_sum` is local to the `_ready()` function.
