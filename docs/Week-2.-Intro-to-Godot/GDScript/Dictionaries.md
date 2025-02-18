---
title: Dictionaries
weight: 7
---

# Dictionaries

In GDScript, a dictionary can be thought of as a container that stores unique keys, as well as different values associated with each of them. It’s similar to an array, but the stored values **do not have a corresponding index**. Instead, you can look up a particular **value** by searching for its **<u>key</u>**.

Let’s create a dictionary that holds information about the attributes of a game character by storing key-value pairs in a variable called `Player`. Note that the dictionary definition can be declared either inside a function (e.g. `func _ready`) or outside any of the functions in the script. The print statements should be included within a function.

```gdscript
var Player = {"Type": "Wizard", "Age" : "500", "Strength" : "Magic", "Weakness" : "Silver"}
print(Player.Type)
print(Player.Age)
print(Player.Strength)
print(Player.Weakness)
```

**Output**

```
Wizard
500
Magic
Silver
```

In this example,

- `Type` is the key, `Wizard` is the value.

- `Age` is the key, `500` is the value.

- `Strength` is the key, `Magic` is the value.

- `Weakness` is the key, `Silver` is the value.

As shown in the example, we can print every element of the dictionary by accessing it using `dictionary_name.key` and replacing `dictionary_name` with the name of the dictionary and key with the name of the key linked to the particular element we want to access.

For instance, we can use `Player.Strength` to get the value `Magic`. We get the same result if we use `Player ["Strength"]`.

Let’s look at some of the things we can do with dictionaries. Note that the code shown in the following examples (1 to 5) should be included within a function (e.g. `func _ready`), and properly indented.

#### 1. Check if it is completely empty

```gdscript
if Player.empty():
      print("The dictionary is empty!")
else:
      print("It's not empty")
```

**Output**

`It's not empty`

---

#### 2. Check the number of elements

```gdscript
Check the number of elements.
var num_elements = Player.size()
print(num_elements) # displays the number of values stored
```

**Output**

`4`

---

#### 3. Check if it contains a particular key

```gdscript
if Player.has("Hobby"):
      print("The key called Hobby exists")
else:
      print("No such key exits in this dictionary")
```

**Output**

`No such key exists in this dictionary`

---

#### 4. Print all the keys

```gdscript
var all_keys = Player.keys() #keys() returns all the keys
print(all_keys)
```

**Output**

`[Type, Age, Strength, Weakness]`

---

#### 5. Print all elements

```gdscript
var elements = Player.values()
print(elements)
```

**Output**

`[Wizard, 500, Magic, Silver]`

---

#### 6. Add items

```gdscript
func new_item (key,element_value):
       Player[key] = element_value
       print("The added key is: ",key)
       print("The added value is: ",Player[key])
       print("Updated dictionary: ",Player)
func _ready():
       new_item("Fav_Food", "pizza")
```

**Output**

```
The added value is: pizza
Updated dictionary: {Age:500, Fav_Food:pizza, Strength:Magic, Type:Wizard, Weakness:Silver}
```

`Fav_Food` is the key, and pizza is the value that is passed to `new_item()` from `_ready()`.
