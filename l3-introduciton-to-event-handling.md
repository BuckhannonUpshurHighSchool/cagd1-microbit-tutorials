# Lesson 3 - Introduction to Event Handling

If you need to see the sample code, press the hint button for each step.


This lesson introduces:
* Basic event handling of button presses
* Display of directional arrows
* Display a custom pattern on the LED 

## Create Event Hanlder for Button A Pressed
Grab the ``||input:on button pressed||`` code block from the 
``||input:Input||`` category in the Toolbox. Leave ```Button.A``` as the 
button pressed.
```typescript
input.onButtonPressed(Button.A, function(){

})
```
## Show the West Arrow 
Grab the ``||basic:show arrow||`` code block from the 
``||basic:Basic||`` category in the Toolbox. Change ``North`` to ``West``, 
and place the code inside the ``onButtonPressed`` event handler.
```typescript
input.onButtonPressed(Button.A, function(){
    basic.showArrow(ArrowNames.West)
})
```
## Create the Event Handler for Button B Pressed
Grab the ``||basic:show arrow||`` code block from the ``||basic:Basic||`` 
category in the Toolbox, and change ``Button.A`` to ``Button.B``.
```typescript 
input.onButtonPressed(Button.B, function(){
    
}) 
```
## Information
The LED on/off indicators should be placed in a grid like the one shown below. 
A ```.``` indicates the led light in that position should be off; whereas, a 
````#```` indicates the led light in that position should be on. The string 
is enclosed in a pair of back tick marks ``` ` ```. The back tick is found above the 
tilde ```~``` on the keyboard.
```typescript
. . . . .
. . . . .
. . # . . 
. . . . .
. . . . .
```
## Display a Custom LED pattern
Grab the ``||basic:show leds||`` code block from the ``||basic:Basic||`` 
category in the Toolbox and place the code inside the event handler 
Button B pressed and change the pattern as shown in the code below: 
```typescript 
input.onButtonPressed(Button.B,function(){
    basic.showLeds(`
    . . # . .
    . . . # .
    # # # # # 
    . . . # .
    . . # . .
    `)
})
```

## Simulate then Download 
Please execute your code within the simulator by interacting with 
the buttons displayed on your screen. For future reference, 
you may also implement an event handler for simultaneous 
presses of the A and B buttons by utilizing ```Button.AB```.

## Notebook Prompts
What is an event in programming?  
What does this code do?
```typescript
input.onButtonPressed(Button.A, function () {
  basic.showIcon(IconNames.Happy)
})
```
Add your own event below that shows a different icon:  
How might this be useful in a real-world device?  
