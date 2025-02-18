---
title: Variables and Data Types
weight: 1
---

# Variables and Data Types

A variable is an entity that can store data values. In Godot, it is represented by the keyword var. Every variable is associated with a data type that tells us the nature of the stored value. Different data types include **integer**, **float**, **Boolean**, and **string**. Let’s take a look at them.

#### Integer

- An integer is a whole number and can be positive, negative, or zero.

- It is represented by the keyword int.

- Examples: 5, 12, 1000, -25, 0, -500

#### Float

- A float is a fractional number that includes a decimal point.

- It is represented by the keyword float.

- Examples: 5.0, 12.4, 0.0002

#### Boolean

- Boolean represents two conditions: true and false.

- It is represented by the keyword bool.

#### String

- A string represents a word, sentence, or continuous series of characters or numbers enclosed within quotes ("").

- Examples: **"M"**, **"ABCD"**, **"1234"**, **"This is a string"**

## Declaring a Variable

Variables are used to store values that may change throughout your code. You can use them to store data related to your game, such as a player’s score, the current game level, and the speed of an object. To declare a variable, write the keyword `var`, followed by an **identifier**, that is, the **name** you want to give the variable. You can choose to assign a value to the identifier either during variable declaration, or in some other part of the code.

In GDScript, identifiers can include any combination of uppercase and lowercase alphabets, an underscore (_), and the digits 0 to 9. Identifiers **cannot start with a digit** and are **case-sensitive**. This means you can call a variable `Emily1234` but not `1234Emily`. Also, `emily` and `Emily` are considered to be two different string values. Here are some examples of variable declarations:

1. `var player_name = "Eva"`

2. `var score = 150`

3. `var player_on_ground = true`

4. `var distance = 10.5`

5. `var total`

### Explicit and Inferred Typing

When declaring a variable, you can choose to specify its type optionally.

Here are some examples:

1. `var fruit: String = "Pineapple"`

2. `var fruit = "Pineapple"`

In each of these cases, you store a string called **"Pineapple"** in the variable `fruit`. But in the first case, you **directly** state that the value you are storing is a **string**, while in the second case, this is inferred. The first method is called **explicit typing**, while the second is called **inferred typing**.

## Constants

**Constants** are values that don’t change when you run a game. When you declare a variable as a constant, its value stays the same throughout the code, and it can’t be assigned any other value.

Here’s an example:

`const LENGTH = 10`

`const SPEED: int = 100`

## Enums

An enum is a group of constants and can be useful when you want each constant to be associated with a consecutive integer. An enum can be written in multiple ways. Here are some examples:

1. ```gdscript
   const CIRCLE = 0
   const SQUARE = 1
   const RECTANGLE = 2
   const TRIANGLE = 3
   ```

2. This can also be written as:

```gdscript
enum Shapes = {CIRCLE, SQUARE, RECTANGLE, TRIANGLE}
const Player = {IDLE = 0, RUN = 3, JUMP = 4}
```

Which can also be written as:

```gdscript
enum Player {IDLE, RUN = 3, JUMP}
```

Values can be accessed by `Player.IDLE`, `Player.RUN`, `Player.JUMP`.

## Keywords

Every programming language has specific words called keywords that are reserved. These should not be used as identifiers, as they hold a special meaning to the compiler. The following are some of the popular keywords of GDScript:

| `if`     | `elif`    | `else`       | `for`      |
| -------- | --------- | ------------ | ---------- |
| `while`  | `match`   | ` break`     | `continue` |
| `pass`   | `return`  | `class_name` | `extends`  |
| `var`    | `const`   | `enum`       | `func`     |
| `static` | `onready` | `export`     | `signal`   |
| `is`     | `as`      | `self`       | `tool`     |

You can read more about these keywords from [Godots official documentation on it](https://docs.godotengine.org/en/stable/tutorials/scripting/gdscript/gdscript_basics.html#keywords).

## Comments

When you want to add comments in your code, you can do so by writing `#` followed by the comment. These are ignored by the engine.

`# This is an example of a comment`

## Output

When you want to display a message or a variable value in the output, you can use the print statement. You have to specify the text to be displayed within the quotation marks and the variable value to be displayed after a comma. Examples include the following:

1. `print("This is being displayed at the output!")`

2. `print("The total Sum= ",sum)`

3. `print(my_variable)`
