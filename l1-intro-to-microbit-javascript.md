# Lesson 1 Introduction to micro:bit and JavaScript

If you need to see the sample code, press the hint button for each step.

## Overview
In this lesson you will:
* Learn the basics of the Micro:bit
* Create your first code in JavaScript 
* Download to your micro:bit 

## Show Happy Icon  

Use the basic ``||basic: show icon||`` function to display the **HAPPY** 
icon. Type the code below, or drag a code snippet from the ``||basic:Basic||`` 
Toolbox category.

```typescript
basic.showIcon(IconNames.Happy)
```

## Clear Screen and Pause

Use the ``||basic:clear screen||`` function followed by the ``||basic:Basic||`` 
function to turn off the light for ```500``` milliseconds (or half a second).

```typescript
basic.showIcon(IconNames.Happy)
basic.clearScreen()
basic.pause(500)
```

## Show the Sad Icon
Copy the code and paste the copy to the end of the existing code.
Change the ```Happy``` to ```Sad``` in the code block
``||basic:show icon||``.

```typescript
basic.showIcon(IconNames.Happy)
basic.clearScreen()
basic.pause(500)
basic.showIcon(IconNames.Sad)
basic.clearScreen()
basic.pause(500)
```

## Run Forever 

Now show the flashing hearts forever by grabbing a 
``||basic:forever||`` block from the ``||basic:Basic||`` category 
in the Toolbox. Then run your code in the Simulator.

```typescript
basic.forever(function()) {
    basic.showIcon(IconNames.Happy)
    basic.clearScreen()
    basic.pause(500)
    basci.showIcon(IconNames.Sad)
    basic.clearScreen()
    basic.pause(500)
}
```
## Download
Click the ``|Download|``  button to download to the micro:bit.

