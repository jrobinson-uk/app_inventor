---
title: Lesson 1 - Activity
layout: page
---

# Lesson 1 - Magic Eight Ball

## Introduction
In this activity you will be creating a magic eight ball app, the idea is that when the user asks a question the magic eight ball will give them a randomly selected answer.

<iframe align="middle" width="840" height="630" src="//www.youtube.com/embed/mFOracFClBg?start=11" frameborder="0" allowfullscreen></iframe>

The original magic eight ball had a range of possible answers which you could use or make up your own.

|Positive|Negative|Neutral|
|--------|--------|-------|
|It is certain|Don't count on it |Reply hazy try again |
|It is decidedly so|My reply is no|Ask again later|
|Without a doubt|My sources say no|Better not tell you now|
|Yes definitely|Outlook not so good|Cannot predict now|
You may rely on it|Very doubtful|Concentrate and ask again|
|As I see it, yes|-|-|
|Most likely|-|-|
|Outlook good|-|-|
|Yes|-|-|
|Signs point to yes|-|-|

## Getting Started
If you have never used app inventor before you may want to visit [http://appinventor.mit.edu/](http://appinventor.mit.edu/) and watch this introduction video.

<iframe width="840" height="630" src="//www.youtube.com/embed/WKM8QCuxmQY" frameborder="0" allowfullscreen></iframe>

<a href="https://drive.google.com/file/d/0B-rfCDlnYkY0SFQzTGxxS0FCWEk/edit?usp=sharing" download="L1a.mp4">Download Video</a>

## :one: Load and test the template

To save time and help you focus on the programming of the magic eight ball some aspects have been completed in advance and saved in a [template](../resources\eightBall.aia) file. Download this file to your computer and follow the steps in the first part of the video to test the app. 

<iframe width="840" height="630" src="//www.youtube.com/embed/d5l50G1n7TM" frameborder="0" allowfullscreen></iframe>
<a href="https://drive.google.com/file/d/0B-rfCDlnYkY0REYyZ3Q3Ymw3U2c/edit?usp=sharing" download="L1b.mp4">Download Video</a>

Currently all the app does is change the image on the button when the button is clicked, the video will also show you how to test the app using the emulator.

<iframe src="//www.youtube.com/embed/_GdEzaB8Xhk" frameborder="0" allowfullscreen></iframe>
<a href="https://drive.google.com/file/d/0B-rfCDlnYkY0cG42UDZDWW5jU0k/edit?usp=sharing" download="L1c.mp4">Download Video</a>

## :two: Displaying a random answer
Continue to watch the video and follow the steps to make the app choose and random answer and display it on the button as text.

1. First you need to set change the text displayed on the button by inserting a **Set EightBall_Button.Image to** block.
2. Then you will want to connect a **pick a random item** block
3. Finally connect an orange **get answers** block
4. Test your app to make sure it works.
5. Expand the apps range of possible answers

## :three: Speaking out loud
Our app would be more impressive if it spoke the answers out to us as well as displaying them as text. The next part of the video show you how to use the **texttospeech** object in app inventor. Do be aware this can only say real words, it won't understand misspelt words.

1. Find the purple **TextToSpeech1.Speak** block and connect below the code that changes the button text.
2. The app will speak out loud whatever is connected to the message connector, add another **pick random item, get global answers** we used earlier.
3. Test the app to ensure it works as expected (ensure you a thorough in your testing)

## :four: Odd behaviour
You probably found that the app didn't quite behave as expected, the text and speech didn't match up? Why was this? Currently our app does this:

1. Changes the images
1. Starts a timer
2. Sets the text to a random answer from the list
3. Read out the text from a random answer from the list.

The problem is that the app picks a random answer twice, these answers could be different and result in different things being displayed and read aloud. This is an example of a **logical** error, the code makes sense to the machine but doesn't do what we thought it would.

To fix the issue we need to pick a random answer once and store that answer in a **variable**. We will then read that variable and use if for the text and the speech.

1. Add an **initialize global** block called *answer* and give it a empty string value (purple " ").
2. In the **button_click** event add an orange **Set global answer** and attach the **pick random item, get global answers**
3. For both the text and the speech replace the **pick random item, get global answers** with an orange **get global answer**
4. Test the changes made to the app.

The next part of the video explains this in more detail.

## :six:  Documenting
You Magic eight ball app is now complete. Something that all good programmers do is to document what there code does. Add to the comments given to you in the template to explain what your app now does.

![](../resources/comments.png)

## :seven: Extending
Now that you have followed the tutorial to create a magic eight ball, lets see if you can add to it. Here are some ideas for extending your app:

- Add your own comment bank to the app.
- Add some sound effects when the app is choosing it's answer
- Fix the app so it's always in portrait mode
- Make it respond to being shaken as well / instead of touching the button. (You will need an **accelerometerSensor**)
 