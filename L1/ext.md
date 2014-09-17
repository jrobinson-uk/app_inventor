---
title: Lesson 1 - Extension
layout: default
---
# Extension Activity 1 - Sound Board

## Introduction

For this extension activity there are no specific guides or videos to aid you, you will be demonstrating that you have understood the key concepts from the [Magic Eightball activity.](student.md).

- You may find the App Inventor [Concept cards](http://appinventor.mit.edu/explore/sites/all/files/ConceptCards/ai2/AI2_ConceptCards.pdf) useful.
- Some sounds and images used in the example app can be found [here](../resources/soundboard.zip).

The aim of the activity is to create a sound board app similar to the one shown in the video clip below.

<iframe src="//www.youtube.com/embed/lAjAINcWyJ4" frameborder="0" allowfullscreen></iframe>
<a href="../resources/L1d.mp4" download="L1d.mp4">Download Video</a>

## Getting Started
Open App Inventor and create a new project choosing a sensible name such as "soundboard".

A successful soundboard app:

- Will have at lease 6 buttons.
- These buttons should fill the screen.
- Each button should have an appropriate label or image.
- When each button is clicked the app will play the relevant sound.
- Could have different behaviours for a click or a long press of the button.


## :one: Arranging the buttons
On your new screen you need add a button for each sound you wish to use to position these buttons you will have to explore the layout tools:

- A **Horizontal layout** will allow you to place objects next to each other.
- A **Vertical layout** will allow you to place objects above and below each other.
- A **Table Layout** can be used to create a grid in which to place other objects
- *Layout tools can be place inside other layout tools to create some complex arrangements.*

You will also need to consider the width and height of each object you insert, there are 3 options:

- **Automatic**, the object will take up as little space as possible and be automatically resized.
- **Fill parent**, the object will take up as much room as it can and will resize automatically.
- **Pixels**, you can specify the exact width or height in pixels and it will not resize.

## :two: Adding sounds
To play a sound you will need to add a **sound** object from the media section of the palette, this will appear as a non-visible component. Any sounds you upload should be:

- Short, the sound player object is designed for short sounds, for longer sounds you should use the **player** object.
- Small in file size, you are limited on space in your app you should use **mp3** files as oppose to **wav** files.

## :three: Adding Images
Upload you images and place one on each button, the images should be small in file size to conserve space, *png* or *gif* are ideal.

## :four: Coding the buttons
The coding for the sound board should be pretty simple you will need a button press event for each button. The event will trigger the loading of the correct sound (by setting the sound objects source) and then playing the sound.

## :five: Extending
This simple sound board app could be extending in a wide range of ways. eg:

- Adding vibration when the buttons are pressed.
- Adding more buttons / screens with more buttons.
- Changing the look of the button whilst it's being pressed.
- Using the longpress event to trigger another behaviour, eg click plays an animal sound and long press says the name of the animal.
