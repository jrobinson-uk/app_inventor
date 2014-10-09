---
title: Lesson 3 - Activity
layout: page
---

# Lesson 3 - Sketchpad

## Introduction
In this activity you will be creating a simple sketchpad app, the idea is that:
- The user can draw points and lines on the canvas.
- The user can slect the desired line thickness and colour.
- The user can take a photo with the camera which can then be drawn on.
- The user can save the image they have created.
- The image can be share using email / twitter etc.

## Getting Started
If you have never used app inventor before you may want to visit [http://appinventor.mit.edu/](http://appinventor.mit.edu/) and watch this introduction video.

<iframe width="840" height="630" src="//www.youtube.com/embed/WKM8QCuxmQY" frameborder="0" allowfullscreen></iframe>

<a href="https://drive.google.com/file/d/0B-rfCDlnYkY0SFQzTGxxS0FCWEk/edit?usp=sharing" download="L1a.mp4">Download Video</a>

## :one: Load and test the template

To save time and help you focus on the programming of the stopwatch some aspects have been completed in advance and saved in a [template](..\resources\Sketchpad_template.aia) file. Download this file to your computer and load it in an emulator or on a device. 

![](../resources/sketchpad.png)

Currently the app has almost all the right objects and layout setup, however there is no code at all. Use the video tutorial below along with the instructions to create your app.

<iframe width="840" height="630" src="//www.youtube.com/embed/rGnFffBh8vk" frameborder="0" allowfullscreen></iframe>


**How to run the emulator**
<iframe src="//www.youtube.com/embed/_GdEzaB8Xhk" frameborder="0" allowfullscreen></iframe>

## :two: Improving the GUI
The Graphical User Interface (GUI) for this app is largely complete but lacks some nice buttons. Find a suitable graphic for each and add them to the app. I found mine on [Icon Finder](https://www.iconfinder.com/browse)
- You could use you own.
- Or download these that I found by [Webalys](https://www.iconfinder.com/iconsets/3_Minicons-Free-_Pack)


## :three: Drawing dots and lines
There are 2 events which we might want to trigger some drawing on the canvas:
- The canvas is touched
- The canvas is dragged

In both we will need to know the x,y co-ordinates of where the canvas was touched in order to make a mark in the right place. The size of the lines in each case will be set by the sliders position.


## :four: Changing Colours
Each time a new colour is selected we want 2 things to happen:
1. Update the colour of the "selected colour" marker to the new colour.
2. Update the colour of the canvas to the new colour.

This can be written something like:

```
when Colour1.click:
	do set Canvas1.PaintColor to Colour1.BackgroundColor
	set Selected_Colour.BackgroundColour to Colour1.BackgroundColor
```

This will need to be repeated for each of the colour buttons.

## :six:  Taking a picture
So we can create some simple drawings, it'd be great if we could take pictures to draw on too. Oh we can? Great!!!
There are 2 events involved in creating this function:

1. The first is the button click, when the button is pressed our app should load the camera app and allow the user to take the picture.
2. The second occurs when the picture has been taken and our app takes over again, the picture that was taken should be set as the canvas background.

## :seven: Clearing, saving & sharing
Three functions remain, the clear button, the save button and finally the sharing button, these are fairly simple functions and can be completed in a few blocks.

**Clearing**

1. Create a button click event for the clear button.
2. Find the Canvas.Clear function and add it (this will only erase the drawing)
3. Set the canvas background image to nothing (give it a empty text block)

**Saving**

1. Create a button click event for the save button.
2. Find a *"call canvas1.SaveAs"* block and attach a text block.
3. The block will *"return"* or tell you the filename where the image was save, we could use this but for now should use a *"evaluate but ignore result"* block.

**Sharing**

1. Create a button click event for the share button.
2. Add a *"Call Sharing1.Sharefile"* block and attach a copy of the *"SaveAs"* block from earlier.
3. This will save the image and pass the image file to the sharing object which can share it.

## :eight: Extending
Now that you have followed the tutorial to create a sketchpad, lets see if you can add to it. Here are some ideas for extending your app:

- Add your own colours.
- Draw other shapes than dots and lines.
- Open existing images to edit.
- Save multiple pictures (currently each save overwrites the previous one.
 
