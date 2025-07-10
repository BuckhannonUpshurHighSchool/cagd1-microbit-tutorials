# Lesson 6 - Buttons and Conditions

## Overview 
This lesson will serve as a 
* Refresher on button events
* Referesher on variables and conditionals in general 
* Introduction to variables in JavaScript 
* Introduction to conditionals in JavaScript
* Introduction to ``||led:Leds||``

## Overview of Tutorial 
This tutorial will show you how to graph a value whose 
input is adjusted by the button presses. Since the screen 
is a 5x5 set of pixels there the value of data being 
graphed is restricted.

## Declare the Variable to be Graphed
To declare a variable grab the ``||variables:let||`` code block 
from ``||variables:Variables||``. Leave the current variable 
name ```item``` as it is. Sometimes you will want to change the 
variable name to make it meaningful about its purpose. Leave its 
type as ```number```.
```typescript 
let item: number 
```
## Initialize the Variable 
Before using a variable it is a good practice to initialize it. 
If it doesn't get initialized, it is possible to get erroneous 
results. Use the ``||variables:equals||`` code block and set ```item``` 
equal to zero. Click on hint to see what the code looks like.
```typescript 
let item: number 
number = 0 
```
## Plot the Variable on a Bar Graph 
To plot a bar graph use the ``||led:plot bar graph||`` code block 
from ``||led:Led||`` category on the Toolbox. Change the first parameter 
to ```item```. This is not a string so do no enclose in double 
quotation marks. Change the secon parameter to ```25```. This will be 
maximum value to be graphed.
```typescript 
let item: number 
number = 0 
led.plotBarGraph(item, 25)
```
## Increase the Variable Value 
This doesn't plot much right now, so add an event handler to 
increase the value of ```item```. Add an event handler from 
``||inputs:Input||`` for button A being pressed. Inside the 
handler, increase the value of ```item``` by 5 using the 
``||Variables:change||`` code block located in the 
``||variables:Variables||`` category in the Toolbox. This 
code should be added at the end.
```typescript 
let item: number 
number = 0 
led.plotBarGraph(item, 25)
input.onButtonPressed(Button.A, function() {
    item += 5
})
```
## Decrease the Variable Value 
Now the increase has been added add an event handler to decrease 
the value of ```item```. This time the event will be button B 
being pressed.
```typescript 
let item: number 
number = 0 
led.plotBarGraph(item, 25)
input.onButtonPressed(Button.A, function() {
    item += 5
})
input.onButtonPressed(Button.B, function() {
    item -= 5
})
```
## Run the Graphing Forever 
Add the ``||basic:forever||`` code block to the end of the current 
code and move the ``||led:plot bar garph||`` command to the inside 
of the loop.
```typescript 
let item: number 
number = 0 
input.onButtonPressed(Button.A, function() {
    item += 5
})
input.onButtonPressed(Button.B, function() {
    item -= 5
})
basic.forever(function() {
    led.plotBarGraph(item, 25)
})
```

## Simulate to Test 
Run the code in the simulator. If you press button A the graph 
continues to grown filling the screen. Then if you press the B 
button, the graph will shrink until there is nothing left. 
There is no way to determine where the value is without 
counting the number of times you press either button.

## Add Code to Prevent the Maximum from Exceeding 25
Insert an ``||logic:if||`` code block after the ``||led:plot bar graph||`` 
code block and inside the ``||basic:forever||`` loop. Change ```true``` 
to ```item > 25``` to check for its value over 25. Then set it equal 
to ```25``` inside the ``||logic:if||`` code block.
```typescript 
let item: number 
number = 0 
input.onButtonPressed(Button.A, function() {
    item += 5
})
input.onButtonPressed(Button.B, function() {
    item -= 5
})
basic.forever(function() {
    led.plotBarGraph(item, 25)
    if (item > 25) {
        item = 25
    }
})
```

## Add Code to Prevent the Minimum from Dropping Below Zero 
Insert an ``||logic:if||`` code block after the previous ``||logic:if||``  
code block and inside the ``||basic:forever||`` loop. Change ```true``` 
to ```item < 0``` to check for its value less than 0. Then set it equal 
to ```0``` inside the ``||logic:if||`` code block.
```typescript 
let item: number 
number = 0 
input.onButtonPressed(Button.A, function() {
    item += 5
})
input.onButtonPressed(Button.B, function() {
    item -= 5
})
basic.forever(function() {
    led.plotBarGraph(item, 25)
    if (item > 25) {
        item = 25
    }
    if (item < 0 {
        item = 0
    }>)
})
```

## Download and Run 
Select ``|Download|`` to download to the micro:bit and test it out.