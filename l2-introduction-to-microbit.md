# Lesson 2 – Intro to micro:bit

## Overview:
In this lesson, you'll create a simple app that scrolls a message across the micro:bit screen.
Before you begin, make sure you've completed the tutorial about the **Simulator**, **Toolbox**, and **Workspace**.

*Need help? Click the **Hint** button on any step for sample code.*

## Step 1 – Add a Comment

At the top of your code, type this comment to describe what your code will do:

`// Declare and initialize myMessage variable`

```typescript
// Declare and initialize myMessage variable 
```

## Step 2 – Declare a Variable

From the ``||variables:Variables||`` category, drag out a ``||variables:let||`` block.
Rename the variable to `myMessage` and change its type to `string` (use camelCase).

```typescript 
// Declare and initialize myMessage variable 
let myMessage: string
```

## Step 3 – Initialize the Variable

Use the ``||variables:equals||`` code block from ``||variables:Variables||`` to 
set `myMessage` equal to a string value of your choice.

```typescript 
// Declare and initialize myMessage variable 
let myMessage: string
myMessage = "Hello! Welcome to micro:bit"
```

## Step 4 – Show the Message

From ``||basic:Basic||``, drag a ``||basic:show string||`` block.
Replace the default text with the variable name:

```typescript 
// Declare and initialize myMessage variable 
let myMessage: string
myMessage = "Hello! Welcome to micro:bit"
basic.showString(myMessage)
```

## Step 5 – Test Your Code

Press **Play** in the Simulator to test it.
Then click ``|Download||` to try it out on your **micro:bit**.
