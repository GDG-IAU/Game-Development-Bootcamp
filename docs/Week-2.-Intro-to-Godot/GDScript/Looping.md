---
title: Looping
weight: 8
---

# Looping

When we want to execute some part of the code multiple times, we use an important programming concept called looping . There are two types of loops in GDScript: **for loops** and **while loops**. Let’s explore each of them with examples.

## For Loop

Let’s look at an example of an array that holds the player’s score during each game level, for a total of four levels. This means that the array stores the player’s level 1 score at index 0, level 2 score at index 1, level 3 score at index 2, and level 4 score at index 3. We can use a for loop for iterating through each of these values.

To access every item in the array, we define our own variable name that points to the current item. Every time the code inside the loop is executed, this variable then points to the next item in the array. In this way, we can access each of the array elements.

```gdscript
extends Node2D
var Level_Score = [0,10,40,60]
var Total_Score = 0
func _ready():
      for current_score in Level_Score:
            Total_Score = current_score + Total_Score
      print("Total score = ", Total_Score)
```

In the example given earlier, we first define an array called `Level_Score` to store the player’s points during each level. We also declare a variable called `Total_Score` for storing the result of the addition of all the elements in this array. Next, use a for loop with an iterative variable called `current_score`, which loops through all the array elements, starting from the element at index 0. After a cumulative addition of all the points inside the for loop, we display the result at the output. We can also use for loops for looping through numerical ranges, strings, and even dictionaries.

Some other examples of for loops include the following:

#### 1. Print all the characters in a string

```gdscript
      func _ready():
            for ch in "GODOT":
                  print(ch)
```

**Output**

```
G
O
D
O
T
```

---

#### 2. Iterate over values from num = 0 to 4

```gdscript
      func _ready():
            for n in 5:
                  print(n)
```

**Output**

```
0
1
2
3
4
```

---

#### 3. Iterate over a range of n = 10 to 15

```gdscript
func _ready():
      for n in range(10,15):
            print(n)
```

**Output**

```
10 
11
12
13
14
```

---

#### 4. Skip certain numbers in an iteration

```gdscript
func _ready():
      for n in range(10,20):
            if(n<=14):
                  continue # values below 15 are not printed
            if(n==18):
                  break # values after 18 are not printed
            print(n)
```

**Output**

```
15
16
```

---

#### 5. Iterate over a dictionary and print all the values

```gdscript
func _ready():
      var player_points = {"P1":10, "P2":50, "P3":80}
      print("Leaderboard: ")
      for key in player_points:
            print(key, " = ", player_points[key], " points")
```

**Output**

```
Leaderboard:
P1 = 10 points
P2 = 50 points
P3 = 80 points
```

## While Loop

We can use while loops in cases where we have to continuously execute some code until a certain condition is reached. Let’s see an example:

```gdscript
extends Node2D
var points = 10
var total_score = 0
func _ready():
      while (total_score <= 200):
            total_score = total_score + points
            print("Total score so far = ", total_score)
            if(total_score == 100):
                  print("You got 100 points! You won!")
                  break
```

In the above example, we have written a while loop for updating the `total_score` continuously by cumulatively adding 10 points to it, until `total_score` reaches a value of 200. The current value of `total_score` is displayed every time 10 more points are added to it. But once the `total_score` reaches a value of 100, the break statement causes the while loop to end, and the statement, `“You got 100 points! You won!”` is displayed in the output.
