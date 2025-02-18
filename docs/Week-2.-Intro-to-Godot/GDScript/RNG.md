---
title: Random Number Generator
weight: 4
---


# Random Number Generation

There are tons of uses for a random number when you’re making a game:

- Spawning a random number of enemies during a game level

- Creating a luck-based computer card game

- Randomly generating elements in the game world, such as the map

- Spawning a random collectible or drop when the player beats an enemy

In GDScript, you can generate random numbers using built-in functions that are based on the concept of pseudorandomness. This means that a number is generated using an algorithm and is thus not truly random. You can easily predict the number if you’re familiar with the algorithm, but this is unlikely. To get a random number, we first need to use the predefined function, `randomize()`, along with another function specific to the type of random number we want. Let’s take a look at how this works.

#### 1 - Random Integer Generation

```gdscript
func _ready():
    var random_int = randi()
    print (random_int)
```

**Output**

`325200109`

The function `randi()` generates a random integer in the range of 0 to 4,294,967,295. If we want to specify our own range, we can do so in the following way.

```gdscript
var rand_generator = RandomNumberGenerator.new()
func _ready():
    var random_int = rand_generator.randi_range(30, 40)
    print(random_int)
```

**Output**

`36`

We first have to declare a new random number generator, e.g., `rand_generator`, and randomize it using the syntax shown earlier. Then, we can use the `randi_range()` function to specify the range of possible values for our random number. In the case shown earlier, a random integer between 30 and 40 is generated.

---

#### 2 - Random Float Generation

```gdscript
func _ready():
    randomize()
    var random_float = randf()
    print (random_float)
```

**Output**

`0.278825`

The `randf()` function generates a random float between 0 and 1. If we want to specify the range of values, we can do it as follows:

```gdscript
func _ready():
      rand_generator.randomize()
      var random_float = rand_generator.randf_range(-1.5,5.0)
      print (random_float)
```

**Output**

`4.950228`

Here, we use `randf_range()` to specify our possible range of float values. The example shown earlier generates a random float value between -1.5 and 5.0.
