---
title: Jupyter Notebook
subtitle: Katelyn Gelle
cover-img: /assets/img/swordplaylink.gif
thumbnail-img: /assets/img/heartlink.jpg
share-img: /assets/img/heartlink.jpg
gh-repo: jellinki/jellyblog
gh-badge: ['star', 'fork', 'follow']
tags: ['test']
comments: True
---

## Python Tutorial

So, what is Python?  
Python is a programming language that can be used to build websites, automate tasks, and conduct data analysis. It has a simplistic appearance, which makes it easier to learn and understand; as such, many beginners start off with "Python" in order to learn the basics of code. Its variety of possible purposes also make it a versatile language in the coding world!  

Let's start off with a Python kernel below:


```python
print("hello world")
```

    hello world


Look, that was pretty fun! Let's see what else we can do with Python:


```python
import random
n = random.randrange(1,10)
guess = int(input("guess a number: "))
while n!= guess:
    if guess < n:
        print("oops, too low!")
        guess = int(input("try again: "))
    elif guess > n:
        print("oh no, too high!")
        guess = int(input("try again: "))
    else:
      break
print("great job, you got it!")
```

Okay, above, this is a short program that is a sort of guessing-game. The player can guess one of the computer's randomly generated numbers from 1 to 10. The program relies heavily on conditional statements such as "if", "elif", and "else". The "if" function poses a question to the computer to which it can reply with a response; these responses can be further developed through "else" (an outcome besides "if") "elif" (a secondary outcome besides else). In this particular program, if the player guesses a number that is too low, the "if" statement allows the computer to tell the player the guess is too low a value and prompts them to try again. The "elif" statement allows the computer to tell the player the guess is too high a value and prompts them to try again. Lastly, if the player guesses "else"--a number that is neither too low nor too high, in other words the perfect and correct number--the computer will tell the player that they are correct and commend them.  

Let's try another example, this time a little more complex:


```python
import random

class Character:
    def __init__(self, name, health, attack, defense):
        self.name = name
        self.health = health
        self.attack = attack
        self.defense = defense

    def take_damage(self, damage):
        actual_damage = max(5, damage - self.defense)
        self.health -= actual_damage
        print(f"{self.name} takes {actual_damage} damage!")

    def is_alive(self):
        return self.health > 0
    
    def is_dead(enemy):
        enemy.health <= 0

def main():
    enemy_templates = [
        ("orc", 50, 10, 5),
        ("thief", 60, 20, 30),
        ("troll", 70, 8, 8),
        ("jelly", 30, 10, 4),
        ("hellhound", 150, 30, 10),
        ("demon", 100, 35, 5),
        ("serpent", 35, 10, 2),
        ("wolf", 50, 10, 5),
        ("skeleton", 40, 10, 1),
        ("zombie", 50, 15, 20),
        ("lich", 150, 30, 50),
        ("doppelganger", 100, 15, 10),
        ("barbarian", 100, 40, 15)
    ]

    while True:  # this makes me replay :)
        player = Character("hero", health=100, attack=15, defense=10)
        enemy_template = random.choice(enemy_templates)  # random enemy template
        enemy = Character(*enemy_template)  # create new enemy instance LFGGG

        print("welcome to bad angband!")
        print(f"whoa, you encounter a {enemy.name}!")

        player_turns = 0  # player can track turns!

        while player.is_alive() and enemy.is_alive():
            player_turns += 1  # increment player turns counter!!!

            # can we heal every five turns????!!!! and MAGIC EVERY SEVEN????
            if player_turns % 5 == 0:
                heal_option = input("your healing potion has replenished. heal now? (yes/no): ").lower()
                if heal_option == "yes":
                    player.health = min(player.health + 25, 100)  # ensure health doesn't exceed 100
                    print("a green aura washes through your system... you feel rejuvenated!")

            if player_turns % 7 == 0:
                magic_option = input("your mana has replenished. use magical attack? (yes/no): ").lower()
                if magic_option == "yes":
                    magical_damage = 25
                    enemy.health -= magical_damage
                    print("blue energy floods through your body... power blasts your enemy!")
                    print(f"critical hit! the {enemy.name} takes 25 damage!")

            action = input("attack, run, or cry? ").lower()
            if action == "attack":
                player_attack = random.randint(1, player.attack)
                enemy_attack = random.randint(1, enemy.attack)

                enemy.take_damage(player_attack)
                player.take_damage(enemy_attack)
            elif action == "run":
                print("you run away!")
                break
            elif action == "cry":
                enemy_attack = random.randint(1, enemy.attack)
                player.take_damage(enemy_attack)
            else:
                print("oops, can't do that! type 'attack', 'run', or 'cry'.")

            print(f"your health: {player.health}")
            print(f"enemy health: {enemy.health}")

        if player.is_alive():
            print(f"congratulations! you defeated the {enemy.name}!")

        elif enemy.is_dead():
            print(f"congratulations! you have defeated the {enemy.name}!")
        else:
            print("you were defeated. womp womp!")

        replay = input("wanna play again? (yes/no): ").lower()
        if replay != "yes":
            print("thanks for playing! farest thee well, adventurer! :D")
            break

if __name__ == "__main__":
    main()
```

This one is a work-in-progress that I call Bad Angband; it's a far more simplistic version of the text-based RPG Angband, a game based off of the lore from *The Lord of the Rings*. Here, players can encounter various monsters of different levels of health, attack, and defense, and can resort to melee attacks, mana restoration, and magical attacks in order to defeat their adversaries. However, I'm working on the magical damage; for some reason, it won't autokill the enemy once they're at 25 hitpoints. It isn't much of an obstacle, as the player can simply take them down the next turn with a basic melee attack, but it's still inconvenient. I'll find a way around it soon, though! :D


```python
print("Link says 'you're doing great!'. Just kidding, he doesn't speak.")
```

![Heart Link](/assets/img/heartlink.jpg "Hyah!"){: .mx-auto.d-block :}
