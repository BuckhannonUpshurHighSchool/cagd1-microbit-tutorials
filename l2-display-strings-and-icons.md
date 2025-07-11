# Lesson 2 - display Strings and Icon Names 

## Overview:
In this lesson (based on the Name Badge tutorial), you will:
* Learn how to scroll text and numbers on the micro:bit 
* Respond to a few reflection questions in your notebook  
*Need help? Click the __Hint__ button on each step*

## Step 1 - How Scrolling Works 
Letters or numbers that are longer than one character will 
**scroll** across the screen automatically.

## Step 2 - Start Your Name Badge 
From the ``||basic:Basic||`` category, drag a ``||basic:show string||`` block.  
Change the text to: `"My name is: "`  
Then drag another `show string` block and change it to 
your **first name**.
```typescript 
basic.showString("My name is: ")
basic.showString("Mrs. Jones)
```

## Step 3 - Clear and Scroll More Text 
Add a ``||basic:clear screen||`` and add another ``||basic:show string||``block and 
change `"Hello!"` to `"My age is: "`. 
```typescript 
basic.showString("My name is: ")
basic.showString("Mrs. Jones")
basic.clearScreen()
basic.showString("My age is: ")
```

## Step 4 - Scroll a Number 
From ``||basic:Basic||``, drag a ``||basic:show number||`` 
block.  
Change the number to your **age**.
```typescript 
basic.showString("My name is: ")
basic.showString("Mrs. Jones")
basic.clearScreen()
basic.showString("My age is: ")
basic.showNumber(62)
```

## Step 5 - Loop It Forever
Drag a ``||basic:forever||`` block from ``||basic:Basic||``.  
Put **all your code** inside it so yur badge loops nonstop.
```typescript 
basic.forever(function(){
    basic.showString("My name is: ")
    basic.showString("Mrs. Jones")
    basic.clearScreen()
    basic.showString("My age is: ")
    basic.showNumber(62)
})
```

## Step 6 - Test Your Badge 
Press **Play** on the simulator to test your code.  
Then click ``|Download|`` to try it on your micro:bit. 

## Step 7 - Notebook Prompts
Answer these questions in your notebook:
1. What are the two main views in MakeCode?
2. What does `basic.showIcon(IconNames.Heart)` do?
3. How do you show a string in JavaScript on the LED display?
4. What's your favorite line of code from this lesson?