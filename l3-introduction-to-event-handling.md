# Lesson 3 - Introduction to Event Handling

## Overview 
In this lesson, you'll: 
* Learn how event handling works 
* Respond to button presses
* Show arros and a custom LED pattern  
*Need help? Click the __Hint__ button on each step to see example code.*

## Step 1 - Handle Button A Press 
From the ``||input:Input||``, drag a ``||input:button pressed||`` block.  
Use the default: **Button A**.
```typescript 
input.onButtonPressed(Button.A, function(){

})
```

## Step 2 - Show a Left Arrow
From the ``||basic:show arrow||`` category, drag a ``||basic:show arrow||``.  
Change the arrow direction to `West` and place it **inside** 
the Button A event handler.
```typescript 
input.onButtonPressed(Button.A, function(){
    basic.showArrow(ArrowNames.West)
})
```

## Step 3 - Handle Button B Press 
Add another ``||input:button pressed||`` block from ``||input:Input||``.  
Change it to **Button B**.
```typescript 
input.onButtonPressed(Button.B, function(){

})
```

## Step 4 - Understand LED Patterns 
The ``||basic:show leds||`` block uses a **5x5 grid** where: 
* `#` = LED ON 
* `.` = LED OFF  
Wrap the pattern in **backticks** if you're typing in JavaScript.

## Step 5 - Show a Custom Pattern 
From ``||basic:Basic||``, drag a ``||basic:show leds||`` block 
into the **Button B** event handler.  
Edit the grid to look like a **right arrow**.
```typescript 
input.onButtonPressed(Button.B, function(){
    basic.showLeds(`
    . . # . .
    . . . # .
    # # # # #
    . . . # .
    . . # . .
    `)
})
```

## Step 6 - Test Your Code 
Click the **simulator buttons** to test both Buttons A and B.  
Tip: You can also add an event for **Button A+B** together using `Button.AB`.

## Step 6 - Notebook Prompts
Answer the following in your notebook:
1. What is an **event** in programming?
2. What does this code do?  
`input.onButtonPressed(Button.A, function() {
    basic.showIcon(IconNames.Happy)
})`
3. Add your own event below that shows a **different icon**.
4. How could event handling be useful in a **real-world device**?