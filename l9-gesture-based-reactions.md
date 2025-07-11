## Lesson 9 – Gesture-Based Reactions

## Overview
In this lesson, you'll create an interactive program that responds to different micro\:bit gestures using a **forever loop** and **if-else conditions**. Based on how the device is moved, it will show different icons or clear the screen.

You will:

* Use gesture input to control outputs
* Display different icons based on how the micro\:bit is held or moved
* Reflect on how gestures compare to button presses

💡 *Need help? Press the **Hint** button on each step to see sample code.*

## Step 1 – Show a Starting Image
Show a happy face or any icon to let the user know the program has started.
```typescript
basic.showIcon(IconNames.Happy)
```

## Step 2 – Add a Forever Loop

From the ``||basic:Basic||`` category, drag out a ``||basic:forever||`` block.
All gesture checks will go inside this loop so the program keeps running.

## Step 3 – Respond to Shake Gesture

Inside the `forever` loop, add an ``||logic:if||`` statement to check if 
the gesture input is a shake: this is accomplished by replacing `true` with 
a ``||input:is gesture||`` block. Display an icon of your choice.
```typescript
if (input.isGesture(Gesture.Shake)) {
  basic.showIcon(IconNames.Ghost)
}
```

## Step 4 – Add Tilt Left Gesture

Add an `else if` to check for a tilt gesture and display a different 
icon of your choice.
```typescript
else if (input.isGesture(Gesture.TiltLeft)) {
  basic.showArrow(ArrowNames.West)
}
```

## Step 5 – Add Tilt Right Gesture

Add another `else if` for a tilte right gesture.
Display another icon of your choice
```typescript
else if (input.isGesture(Gesture.TiltRight)) {
  basic.showArrow(ArrowNames.East)
}
```

## Step 6 – Add Logo Up Gesture

Continue your conditions with checking of the logo is up.
```typescript
else if (input.isGesture(Gesture.LogoUp)) {
  basic.showIcon(IconNames.Yes)
}
```

## Step 7 – Add Logo Down Gesture

Add another condition for down gesture:

```typescript
else if (input.isGesture(Gesture.LogoDown)) {
  basic.showIcon(IconNames.No)
}
```

## Step 8 – Clear Screen If No Gesture

Finish the `if-else` chain with clearing the screen.  
This ensures that if no gesture is detected, the screen goes blank.

```typescript
else {
  basic.clearScreen()
}
```

## Step 9 – Test Your Program

Run your program in the **simulator** or download it to your **micro\:bit**.
Try each gesture: shake, tilt left/right, logo up/down. Watch the icons change!

## Step 10 – Notebook Reflection

Answer the following in your notebook:

1. What gesture(s) did you use in your program?
2. What outputs (LEDs or sound) did you connect to gestures?
3. How do gesture events differ from button events?
4. Why might someone use gestures instead of buttons in a real-world device?
