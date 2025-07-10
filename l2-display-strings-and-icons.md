# Lesson 2 - Display Strings and IconsNames 

If you need to see the sample code, press the hint button for each step.

## Overview
In this lesson you will:
* Complete a tutorial for scrolling strings and numbers 
* Respond to a notebook prompts about this lesson

## Information
When displaying a single character or digit, there is no 
scrolling involved. However, if the text or number exceeds 
one character or digit, it will scroll across the screen 
accordingly.

## Start a name badge 
Grab the ``||basic:show string||`` code block from the ``||basic:Basic||`` 
category in the Toolbox, and change ```"Hello!"``` to ```"My name is: ```. 
Then drag a second ``||basic.show string||`` code block below that and 
change ```"Hello!"``` to your name.  
**Note: ** Text is contained inside two double quotes.
```typescript
basic.showString("My name is: ")
basic.showString("<your first name goes here>")
```
## Clear Screen and Scroll Another Text 
Grab the ``||basic:clear screen||`` and ``||basic:show string||`` 
code blocks from the ``||basic:Basic||`` category in the Toolbox, and change
```"Hello!"``` to ```My age is: ```.
```typescript
basic.showString("My name is: ")
basic.showString("<your first name goes here>")
basic.clearScreen()
basic.showString("My age is: ")
```
## Scroll a Number 
Grab the ``||basic:show number||`` and change ```0``` to your age.  
**Note: ** Numbers are not contained inside double quotes.
```typescript
basic.showString("My name is: ")
basic.showString("<your first name goes here>")
basic.clearScreen()
basic.showString("My age is: ")
basic.showNumber(<your age goes here>)
```

##Scroll Forever
Grab the ``||basic:forever||`` loop from the the ``||basic:Basic||`` category 
in the Toolbox and place your code inside the loop.
```typescript
basic.forever(function() {
    basic.showString("My name is: ")
    basic.showString("<your first name goes here>")
    basic.clearScreen()
    basic.showString("My age is: ")
    basic.showNumber(<your age goes here>)
})
```
## Simulate
Press play on the simulator. Then press ``|Download|`` to download and test on 
the micro:bit.

## Notebook Prompts

What are the two main views in MakeCode?  
What does ```basic.showIcon(IconNames.Heart)``` do?  
In JavaScript, how do you show a string message on the LED display?  
Write your favorite line of code from this lesson:
