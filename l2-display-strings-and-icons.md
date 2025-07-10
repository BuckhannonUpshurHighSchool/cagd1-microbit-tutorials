# Lesson 2 - Display Strings and IconsNames 

## Overview
In this lesson you will:
* Complate a tutorial for scrolling strings and numbers 
* Respond to a notebook prompt about this lesson
* Create a name badge for the micro:bit

## Information
When displaying a single character or digit, there is no 
scrolling involved. However, if the text or number exceeds 
one character or digit, it will scroll across the screen 
accordingly.

## Scroll text 
Grab the ``||basic:show string||`` code block from the ``||basic||`` 
category in the Toolbox, and change ```"Hello!"``` to ```"Coding 1"```.  
**Note: ** Text is contained inside two double quotes.
```typescript
basic.showString("Coding 1")
```
## Clear Screen and Scroll Another Text 
Grab the ``||basic:clear screen||`` and ``||basic:show string||`` 
code blocks from the ``||basic||`` category in the Toolbox, and Change
```"Hello!"``` to ```"Room "```.
```typescript
basic.showString("Coding 1")
basic.clearScreen()
basic.showString("Room ")
```
## Scroll a Number 
Grab the ``||basic:show number||`` and change ```0``` to ```103```.  
**Note: ** Numbers are not contained inside double quotes.
```typescript
basic.showString("Coding 1")
basic.clearScreen()
basic.showString("Room ")
basic.showNumber(103)
```
## Simulate
Press play on the simulator.

## Notebook Prompt

In JavaScript, how do you show a string message on the LED display?

## Create a Name Badge 
1. Create a New JavaScript Project .
2. Scroll ```"My name is: "``` followed by your first name.
3. Scroll ```"My age is: "``` follwed by your age as a number.
4. Test in the simulator.
5. Download to the micro:bit