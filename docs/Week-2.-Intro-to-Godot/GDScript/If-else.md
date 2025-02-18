---
title: If-else Statements
weight: 6
---

# If-else Statements

Whenever we want to set certain conditions before executing a block of code, we can write if-else statements . We use these statements when we want to tell the computer, “**If** something happens, **then** do this; **else** do something else.” The keyword if checks whether a certain condition is true and executes a certain portion of code if it is. If it’s not, then we can check whether other conditions are true using **elif** statements and specify the corresponding blocks of code that need to be executed for each particular case. If none of the conditions is true, the code specified under the else condition is executed.

Whenever we want to set certain conditions before executing a block of code, we can write if-else statements . We use these statements when we want to tell the computer, “If something happens, then do this; else do something else.” The keyword if checks whether a certain condition is true and executes a certain portion of code if it is. If it’s not, then we can check whether other conditions are true using elif statements and specify the corresponding blocks of code that need to be executed for each particular case. If none of the conditions is true, the code specified under the else condition is executed.

#### SNIPPETS OF SYNTAX

Let’s take a gaming scenario to see this logic in action:

**If a player’s health is below or equal to 10%, the player needs to collect one healing powerup to increase health to 50% and two healing powerups to increase health to 100% to continue playing the game. But if the player doesn’t collect any powerups and the player’s health falls to 0, the game is over.**

This can be represented by the following code:

```gdscript
extends Node2D
var health = 100 # Initial value that will change in the game
var powerup
func _ready():
      if health <= 10:  # Check if Player's health is below or equal to 10 %
            if powerup == 1:
                  print("You got one power-up! Health= 50%")
            elif powerup == 2:
                  print("You got two power-ups! Health= 100%")
            else:
                  print("Gameover!!")
      else:
            print("Health is more than 10%, you're safe")
```
