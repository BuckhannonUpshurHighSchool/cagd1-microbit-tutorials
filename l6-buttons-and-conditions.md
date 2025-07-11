# Lesson 6 - Buttons and Conditions

## Overview 
In this lesson, you'll build a simple graph that increases or 
decreases using button presses.  
You will: 
* Review how button events and conditionals work
* Learn how to use variables and `if` statements in JavaScript 
* Keep your graphed value between 0 and 25  
*Need Help? Press the __Hint__ button for sample code.*

## Step 1 - Declare a Variable 
From the ``||variables:Variables||`` category, drag a ``||variables:let||`` 
block to create a variable.  
Keep the name `item` for now.
```typescript 
let item: number
```

## Step 2 - Initialize the Variable 
Use the ``||variables:equals||`` block from the ``||variables:Variables||`` 
to set `item = 0`.  
This makes sure it starts with a clean value.
```typescript 
let item: number
item = 0
```

## Step 3 - Plot a Bar Graph 
From ``||led:Led||``, drag the ``||led:plot bar graph||`` block. 
* Set the first value to `item` 
* Set the max value to `25` 
```typescript 
let item: number
item = 0
led.plotBarGraph(item, 25)
```

## Step 4 - Increase the Value 
Add a ``||input:run code on button pressed||`` event from ``||input:Input||``.
Inside it, use the ``||variables:change||`` block to change `item` by 5 
from ``||variables:Variables||``. 
```typescript 
input.onButtonPressed(Button.A, function(){
    item += 5
})
```

## Step 5 - Decrease the Value 
Add a ``||input:run code on button pressed||`` event for **Button B**.
Inside it, use ``||variables:change||`` `item` by -5 to decrease the value.
```typescript 
input.onButtonPressed(Button.B, function(){
    item -= 5
})
```

## Step 6 - Loop the Graphing
Add a ``||basic:forever||`` block from ``||basic:Basic||``.  
Move your `plot bar graph` block into this loop to keep it updating.
```typescript 
let item: number
item = 0

input.onButtonPressed(Button.A, function(){
    item += 5
})

input.onButtonPressed(Button.B, function(){
    item -= 5
})

basic.forever(function(){
    led.plotBarGraph(item, 25)
})
```

## Step 7 - Test the Code 
Press **Play** in the simulator.
* Press **A** to grow the graph 
* Press **B** to shrink it  
Right now the value can go too high or too low. Let's fix that.

## Step 8 - Set a Max Limit 
Inside the `forever` loop, after the graph: 
* Add an ``||logic:if||`` block
* Set the condition to `item > 5` 
* Inside it, set `item = 25`
```typescript 
basic.forever(function(){
    led.plotBarGraph(item, 25)
    if (item > 25){
        item = 25
    }
})
```

## Step 9 - Set a Min Limit 
Below the previous `if` block:
* Add another ``||logic:if||`` block 
* Set the condition to `item < 0` 
* Inside it, set `item = 0` 
```typescript 
basic.forever(function(){
    led.plotBarGraph(item, 25)
    if (item > 25){
        item = 25
    }
    if (item < 0) {
        item = 0
    }
})
```

## Step 10 - Download and Try It 
Click ``|Download|`` and run it on your micro:bit.  
Press buttons to grow or shrink the graph - now it stays 
between 0 and 25!
