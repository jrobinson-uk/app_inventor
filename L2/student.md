---
title: Lesson 2 - Activity
layout: page
---

# Lesson 2 - Stopwatch

## Introduction
In this activity you will be creating a stopwatch app, the idea is that:
- When the user presses start the timer should be enabled 
- When the stop button is pressed the timer should be disabled
- When the Reset button is pressed the time stored should be cleared
- The time increase the time every tenth of a second and display the current time.

## Getting Started
If you have never used app inventor before you may want to visit [http://appinventor.mit.edu/](http://appinventor.mit.edu/) and watch this introduction video.

<iframe width="840" height="630" src="//www.youtube.com/embed/WKM8QCuxmQY" frameborder="0" allowfullscreen></iframe>

<a href="https://drive.google.com/file/d/0B-rfCDlnYkY0SFQzTGxxS0FCWEk/edit?usp=sharing" download="L1a.mp4">Download Video</a>

## :one: Load and test the template

To save time and help you focus on the programming of the stopwatch some aspects have been completed in advance and saved in a [template](..\resources\Stopwatch_Template.aia) file. Download this file to your computer and load it in an emulator or on a device. 

<iframe width="840" height="630" src="//www.youtube.com/embed/EzavOUMpdPM" frameborder="0" allowfullscreen></iframe>

Currently the app does very little but you should load it, explore how it has been made so far and load it ready in the emulator.

<iframe src="//www.youtube.com/embed/_GdEzaB8Xhk" frameborder="0" allowfullscreen></iframe>
<a href="https://drive.google.com/file/d/0B-rfCDlnYkY0cG42UDZDWW5jU0k/edit?usp=sharing" download="L1c.mp4">Download Video</a>

## :two: Making the timer tick
Continue to watch the video and follow the steps to make the clock.timer event work and the timer tick

1. Add a clock1.timer event to you blocks.
2. Find the value of tenths of second add 1 to it and store the new value back in tenths of seconds or (**Set ts to - get ts + 1**).![](../resources/variable.png)
3. This will count but not display the value, to do this make it set the text of the current_time label to the ts variable.
4. Next you need to enable the timer when start is pressed by adding a "True" block to the "Set clock1.TimerEnabled to" block.
5. Finally you need to make the stop button work in a similar way to the Start.


## :three: Displaying the time nicely
Our display currently is not good as it only shows the number of tenths of seconds since the start, not the seconds, minutes or hours.

1. First create a pink text join block with 7 connectors (one for each variable and 3 separators).
2. Replace the text set to the **Current_time** label with the join block.
3. Connect the hours,minutes,seconds and tenths blocks to the join block with a ":" piece of text between them.
4. Test you app.


## :four: Carrying over the columns
To carry over the tenths of seconds column to seconds we will need to use an if block. 

This if block will ask if the tenths of seconds has reached 9. If is has then it will:
1. set the number of tenths back to 0
2. add 1 to the number of seconds.

Using this method you should be able do the same for the minutes and hours.

## :six:  Reset Button
Nearly there, our reset button needs to do 2 things.
1. Reset each of our timer variables to 0
2. Update the display with the newly reset time
## :seven: Extending
Now that you have followed the tutorial to create a stopwatch, lets see if you can add to it. Here are some ideas for extending your app:

- Currently the timer is a little out due to using tenths of seconds, can you adjust the timer interval to make it more accurate.
- Could you add lap or split functions?
- How would you adapt this app to make a countdown timer instead.
 
