---
title: Array
weight: 3
---

# Array

An ***array*** is a data type that stores a set of variables at different index positions. You can think of it as a set of address locations, with each location holding a different value or variable. Each stored item is called an ***element*** and can be accessed using its index, starting from index 0.

Here’s an example of an array called `Games`, which stores the names of four different video games:

```gdscript
var Games = ["Mario", "Donkey Kong", "Pac-man", "Breakout"]

func _ready():
     print(Games[0])
     print(Games[1])
     print(Games[2])
     print(Games[3])
```

**Output:**

```
Mario
Donkey Kong
Pac-man
Breakout
```

As we see at the output, Mario is stored at index 0, Donkey Kong at index 1, Pac-man at index 2, and Breakout at index 3. Taking this Games array as an example, let’s look at some typical array functions.

#### 1 - Count the number of elements, using `size()`

```gdscript
var num_elements = Games.size()
print(num_elements)
```

**Output**

`4`

Since `Games` has four different items, the output will be 4.

---

#### 2 - Check whether it contains a specific element, using `find()`

```gdscript
print(Games.find("Pac-man"))
```

**Output**

`2`

---

```gdscript
print(Games.find("Ms. Pac-man))
# Checks whether Ms. Pac-man appears in Games
```

**Output**

`-1`

Since Pac-man is present at the index number 2 in `Games`, the output is 2 for this case. On the other hand, since “Ms. Pac-man” is not part of `Games`, we get a value of -1 at the output.

---

#### 3 - Check the number of times an element occurs, using `count()`

```gdscript
var count_element = Games.count("Breakout")
print(count_element)
```

**Output**

`1`

As "Breakout" only appears once in `Games`, the output is 1.

---

#### 4 - Add an item to the end of the array, using `append()`

```gdscript
Games.append("Tron")
print(Games)
```

**Output**

`[Mario, Donkey Kong, Pac-man, Breakout, Tron]`

In this example, we're simply adding **"Tron"** to `Games`.

---

#### 5 - Shuffle the order of the items, using `shuffle()`

```gdscript
randomize()
Games.shuffle()
print(Games)
```

**Output**

`[Donkey Kong, Tron, Breakout, Mario, Pac-man]`
