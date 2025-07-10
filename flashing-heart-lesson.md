## ~ tutorial
## @preferredEditor javascript

# Flashing Heart lesson 

In this lesson you will:
* Learn the basics of the Micro:bit
* Create your first code in JavaScript 
* Download to your micro:bit 
* Respond to  a notebook prompt about the lesson

## Show a Heart Icon 

Use the basic ``||basic: show icon||`` function to display the **HEART** 
icon. Type the code below, or drag a code snippet from the ``||basic||`` 
Toolbox category.

```typescript
basic.showIcon(IconNames.Heart)
```

## Clear Screen and Pause

Use the ``||basic:clear screen||`` function followed by the ``||basic:pause||`` 
function to turn off the light for **500** milliseconds (or half a second).

```typescript
basic.showIcon(IconNames.Heart)
basic.clearScreen()
basic.pause(500)
```

## Show the Small Heart icon.
Copy the code and paste the copy to the end of the existing code.
Change the **Heart** to **SmallHeart** in the code block
``||basic:show icon||``.

```typescript
basic.showIcon(IconNames.Heart)
basic.clearScreen()
basic.pause(500)
basic.showIcon(IconNames.SmallHeart)
basic.clearScreen()
basic.pause(500)
```

## Run Forever 

Now show the flashing hearts forever by grabbing a 
``||basic:forever||`` block from the ``||basic||`` category 
in the Toolbox.

```typescript
basic.forever(function()) {
    basic.showIcon(IconNames.Heart)
    basic.clearScreen()
    basic.pause(500)
    basci.showIcon(IconNames.SmallHeart)
    basic.clearScreen()
    basic.pause(500)
}
```

## Download
Click the **Download**  button to download to the micro:bit.

## Notebook Prompt
What does ```basic.showIcon(IconsNames.Heart)``` do?
