# Lesson 1 - Introduction to micro:bit and JavaScript

## Overview
In this lesson (based on the Flashing Hearts tutorial) you'll:
* Learn how the micro:bit works
* Write your first JavaScript code 
* Download and run it on the micro:bit  
*Need help? Press the __Hint__ botton on each step*

## Step 1 - Show an Icon 
Use `show icon` to display any icon you like.  
Drag it from the ``||basic:Basic||`` category or type the code manually.
```typescript 
basic.showIcon(IconNames.Heart)
```

# Step 2 - Clear Screen and Pause 
After showing the icon, add `clear screen` and then 
`pause` for **500 ms** to turn off the lights for half 
a second.
```typescript 
basic.showIcon(IconNames.Heart)
basic.clearScreen()
basic.pause(500)
```

## Step 3 - Show a Different Icon 
Copy your first `show icon` line and past it below the puase.  
Change it to a **different icon**. Copy the `clear screen` 
and `pause` lines and paste after the new `show icon` line.
```typescript 
basic.showIcon(IconNames.Heart)
basic.clearScreen()
basic.pause(500)
basic.showIcon(IconNames.SmallHeart)
basic.clearScreen()
basic.pause(500)
```

## Step 4 - Run Forever
Wrap your code in a ``||basic:forever||`` block 
(from ``||basic:Basic||``) so it loops continuously.  
Run your code in the **simulator** to test it.
```typescript 
basic.forever(forever() {
    basic.showIcon(IconNames.Heart)
    basic.clearScreen()
    basic.pause(500)
    basic.showIcon(IconNames.SmallHeart)
    basic.clearScreen()
    basic.pause(500)
})
```

## Step 5 - Download to micro:bit 
Click the ``|Download|`` button and send your code to the 
micro:bit.  
Watch your icons flash in a loop.