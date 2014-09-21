---
title: Lesson 2 - Extension
layout: page
---
# Extension Activity 2 - Cookie Clicker Clone

## Introduction

For this extension activity there are no specific guides or videos to aid you, you will be demonstrating that you have understood the key concepts from the [Stopwatch App.](../student.md).

- You may find the App Inventor [Concept cards](http://appinventor.mit.edu/explore/sites/all/files/ConceptCards/ai2/AI2_ConceptCards.pdf) useful.
- You will need to source your own images and sounds for this app.

The aim of the activity is to create simple clicker game (like [cookie clicker](http://orteil.dashnet.org/cookieclicker/))in which the player has to click a button as often as they can in a fixed time (30 seconds). 

## Getting Started
Open App Inventor and create a new project choosing a sensible name such as "clicker".

A successful app:

- Will have a button to click.
- A variable for each of your score and your time.
- Appropriate starting values for you variables
- Somewhere to display the score
- A timer to countdown the time variable.
- Somewhere to display the current time.
- An image for you button.


## :one: Scoring points
Add a button to your first screen and make it a suitable size, remember:

- **Automatic**, the object will take up as little space as possible and be automatically resized.
- **Fill parent**, the object will take up as much room as it can and will resize automatically.
- **Pixels**, you can specify the exact width or height in pixels and it will not resize.

Next configure your blocks so that when the **button is clicked** the **score is increased by 1** and the **score is updated** on the screen.

**Remember to increase a variable you would say :** *set myvariable to myvariable + 1 *

## :two: Counting down
We now need to decrease time, so that the game can be made to end. Your **clock object** has an event called **timer**, in this event you will want to:
- decrease you time variable by 1
- update the time displayed on screen

## :three: Ending the game
If you play your game you will find that it continues to count time below 0 and produces negative numbers, to fix this:
- After your timer decreases the time, as **if** the time left is less than or equal to 0.
- **If** it then stop the timer

## :four: Game Over screen
Can you add a second screen called game over, when the times reaches 0 it should **open another screen** display a game over message. Add a button to take you back the game screen and label it something like "try again".

## :five: Extending
This simple sound board app could be extending in a wide range of ways. eg:

- Display the players score on the game over screen (need to pass a start value)
- Sound effects / music
- Multiple buttons