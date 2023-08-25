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

## XXX Bash Tutorial  

A brief overview of Bash, on your way to becoming a Linux expert. 

So, what is bash used for?
Bash is an application; it can be used to automate software development tasks, which makes things a lot more convenient for programmers. Bash can be used to assess, configure and optimize network performance on organizational networks.  

On another note, let's test out a Python kernel below:


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
