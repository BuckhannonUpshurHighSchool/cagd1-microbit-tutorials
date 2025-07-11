# Lesson 8 – Tilt & Gesture Events

## Overview:
In this lesson, you'll use gesture events to create a step counter.
You will:

* Track steps using the **shake** gesture
* Display and reset the step count
* Add a challenge feature when you reach a goal  
*Need help? Click the __Hint__ button for sample code.*

## Step 1 – Create a Step Counter
Use a ``||variables:let||`` block from ``||variables:Variables||`` to declare a variable 
named `steps`.  
Set `steps = 0` to start.
```typescript 
let steps: number
steps = 0
```

## Step 2 – Add Steps on Shake
From ``||input:Input||``, drag a ``||input:run code on gesture||`` block.  
Change the gesture to **shake**.
Inside the block, increase `steps` by 1.
```typescript
input.onGesture(Gesture.Shake, function(){
    steps += 1
})
```

## Step 3 – Show Step Count on Button B
Add a `Button A pressed` event.
Inside the block, use `show number` to display the `steps` value.
```typescript
input.onButtonPressed(Button.A, function(){
    basic.showNumber(steps)
})
```

## Step 4 – Reset Step Count
Add a `Button B pressed` event.  
Inside the block, set the the counter to 0.
* Then clear the screen.
* Still inside the Button B event:
```typescript
input.onButtonPressed(Button.B, function(){
    basic.clearScreen()
    steps = 0
})
```

## Step 5 – Download and Test
Click ``|Download|`` and test it on the micro\:bit.
Shake to add steps, press **B** to view and reset them.

## Step 6 – Challenge: Add a Goal

Set a **step goal** (e.g., 10 steps).
Inside the Button A event, use an `if` block:

* If `steps >= goal`, show a **smiley face** after displaying the step count.
