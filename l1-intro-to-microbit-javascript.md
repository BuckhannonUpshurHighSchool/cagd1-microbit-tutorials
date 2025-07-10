# Lesson 1 Introduction to micro:bit and JavaScript

## Overview
In this lesson you will:
* Learn the basics of the Micro:bit
* Create your first code in JavaScript 
* Download to your micro:bit 
* Respond to a notebook prompt about the lesson

## Show Happy Icon  

Use the basic ``||basic: show icon||`` function to display the **HAPPY** 
icon. Type the code below, or drag a code snippet from the ``||basic||`` 
Toolbox category.

```typescript
basic.showIcon(IconNames.Happy)
```

## Clear Screen and Pause

Use the ``||basic:clear screen||`` function followed by the ``||basic:pause||`` 
function to turn off the light for **500** milliseconds (or half a second).

```typescript
basic.showIcon(IconNames.Happy)
basic.clearScreen()
basic.pause(500)
```

## Show the Sad Icon
Copy the code and paste the copy to the end of the existing code.
Change the **Happy** to **Sad** in the code block
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
``||basic:forever||`` block from the ``||basic||`` category 
in the Toolbox.

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
Click the **Download**  button to download to the micro:bit.

## Notebook Prompt
What does ```basic.showIcon(IconsNames.Happy)``` do?
