# Lesson 7 - Reaction Timer App

## Overview
Build a reaction timer app on the micro:bit. You'll use variables, conditions, and 
events to measure and display the user's reaction time. Along the way, you'll comment 
your code and answer reflection questions in your notebook.

## Step 1 - Learn How the App Works
This app waits a random time (2-5 seconds), shows an icon, and measures how fast the 
user presses Button A. If they press too early, it's a false start. The app tracks 
the best reaction time while it's running.

## Step 2 - Set Up the Variables
You'll use these six variables:
* `startTime` - when the timer starts
* `endTime` - when Button A is pressed
* `reactionTime` - difference between start and end time
* `waitTime` - random delay before the prompt
* `bestTime` - best reaction time so far
* `falseStart` - tracks if the user pressed too early

## Step 3 - Add a Comment Section for Variables
Add this comment at the top of your code:  
`// Declare the variables`

## Step 4 - Declare the Variables
Use ``||variables:let||`` blocks in the ``||variables:Variables||`` category 
to create these variables:  
`startTime`, `endTime`, `reactionTime`, `bestTime`, `waitTime` (as numbers)  
`falseStart` (as a boolean)
```typescript
// Declare the variables 
let startTime: number
let endTime: number
let reactionTime: number
let bestTime: number
let waitTime: number
let falseStart: boolean
```

## Step 5 - Initialize the Variables
Add this comment after declaring the variables:  
`// Initalize numbers to 0 and boolean to true`  
Then, set all number variables to 0 and falseStart to true.
```typescript
// Initialize numbers to 0 and boolean to true
startTime = 0
endTime = 0
reactionTime = 0
bestTime = 0
waitTime = 0
falseStart = boolean
```

## Step 6 - Add a Forever Loop
At the bottom of your code, add a ``||basic:forever||`` block from ``||basic:Basic||``.  
You'll write the main game logic inside this loop.
```typescript
basic.forever(function() {

})
```

## Step 7 - Comment the Wait Time Logic
Inside the forever block, add a multi-line comment as shown in the Hint.  
```typescript
basic.forever(function() {
    /*
    Set a random wait time
    Display a message
    Pause
    Show an icon
    Start the timer
    */
})
```

## Step 8 - Set the Random Wait Time
Inside the forever block, set `waitTime = randint(2, 5) * 1000`.
This gives a delay between 2 and 5 seconds.
```typescript 
basic.forever(function() {
    /*
    Set a random wait time
    Display a message
    Pause
    Show an icon
    Start the timer
    */
    waitTime = randint(2, 5) * 1000
})
```

## Step 9 - Comment the Start Sequence
Add this single-line comment after the wait time code:  
`// Display start message, pause, show icon, turn off false start, start timer`

## Step 10 - Code the Start Sequence
Still inside the forever loop:  
Show string "Get ready..."  
Pause `waitTime`  
Clear screen  
Show an icon (any you like)  
Set `falseStart = false`   
Set `startTime = ` running time (ms) (found in ``||input:Input...||``)  

```typescript 
basic.forever(function() {
    /*
    Set a random wait time
    Display a message
    Pause
    Show an icon
    Start the timer
    */
    waitTime = randint(2, 5) * 1000

    // Display start message, pause, show icon, turn off false start, start timer
    basic.showString("Get ready...")
    basic.pause(waitTime)
    basic.clearScreen()
    basic.showIcon(IconNames.Happy)
    falseStart = false
    startTime = input.runningTime()
})
```

## Step 11 - Add Event for Button A Pressed
Add a Button A Pressed event handler from ``||input:Input||``.  
Leave it empty for now — you'll add code next.
```typescript 
input.onButtonPressed(Button.A, function(){

})
```
## Step 12 - Comment the Event Logic
Inside the event block, add this comment:  
`// If not a false start, calculate reaction time and update best time`

## Step 13 - Add Outer If Statement
Inside the event, add an ``||logic:if||`` block that checks:  
if `falseStart == false`   
  
Then inside the if:  
Set `endTime =` running time (ms)  
Set `reactionTime = endTime - startTime`
```typescript 
input.onButtonPressed(Button.A, function(){
    // If not a false start, calculate reaction time and update best time
    if (falseStart == false) {
        endTime = input.runningTime()
        reactionTime = endTime - startTime
    }
})
```

## Step 14 - Add Inner If to Update Best Time
Still inside the outer if:  
Add another ``||logic:if||`` block that checks:  
if bestTime == 0 or reactionTime < bestTime  
Inside it, set `bestTime = reactionTime`
```typescript 
input.onButtonPressed(Button.A, function(){
    // If not a false start, calculate reaction time and update best time
    if (falseStart == false) {
        endTime = input.runningTime()
        reactionTime = endTime - startTime
    }
    if (bestTime == 0 || reactionTime < bestTime) {
        bestTime = reactionTime
    }
})
```

## Step 15 - Show Best Time and Reset
After the inner if:  
Show string "Best time: "  
Show number bestTime  
Set falseStart = true  
```typescript 
input.onButtonPressed(Button.A, function(){
    // If not a false start, calculate reaction time and update best time
    if (falseStart == false) {
        endTime = input.runningTime()
        reactionTime = endTime - startTime
    }
    if (bestTime == 0 || reactionTime < bestTime) {
        bestTime = reactionTime
    }
    basic.ShowString("Best time: ")
    basic.showNumber(bestTime)
    falseStart = true
})
```

## Step 16 - Download and Test
``|Download|`` your code to the micro:bit and test your reaction timer!  
Try multiple times and see how your best time improves.

## Step 17 - Notebook Reflection
Answer the following in your notebook:
* How does this app use events and time?
* Which variables store time?
* What was a challenge you faced in this tutorial?
* What feature would you add to make it better?