# Smiley Buttons

## {Introduction @unplugged}

Code the buttons on the @boardname@ to show that it's happy or sad.
(Want to learn how the buttons works? [Watch this video](https://youtu.be/t_Qujjd_38o)).

![Pressing the A and B buttons](/static/mb/projects/smiley-buttons/sim.gif)

## {Step 1}

Use the ``||input:on button pressed||`` block to run code when button **A** is pressed.

```blocks
input.onButtonPressed(Button.A, function() { 
})
```

## {Step 2}

Place a ``||basic:show leds||`` block inside ``||input:on button pressed||`` to display a smiley on the screen. Press the **A** button in the simulator to see the smiley.

```blocks
input.onButtonPressed(Button.A, function() { 
    basic.showLeds(`
        # # . # #
        # # . # #
        . . . . .
        # . . . #
        . # # # .`
        )
})
```

## {Step 3}

Add ``||input:on button pressed||`` and ``||basic:show leds||`` blocks to display a frowny when button **B** is pressed.

```blocks
input.onButtonPressed(Button.B, function() { 
    basic.showLeds(`
        # # . # #
        # # . # #
        . . . . .
        . # # # .
        # . . . #`
        );
});
```

## {Step 4}

Add a secret mode that happens when **A** and **B** are pressed together. For this case, add multiple ``||basic:show leds||`` blocks to create an animation.

```blocks
input.onButtonPressed(Button.AB, function() {
    basic.showLeds(`
        . . . . .
        # . # . .
        . . . . .
        # . . . #
        . # # # .
        `)
    basic.showLeds(`
        . . . . .
        . . # . #
        . . . . .
        # . . . #
        . # # # .
        `)    
})
```

## {Step 5}

If you have a @boardname@, connect it to USB and click ``|Download|`` to transfer your code. Press button **A** on your @boardname@. Try button **B** and then **A** and **B** together.

## {Step 6}

Nice! Now go and show it off to your friends!

```template
input.onButtonPressed(Button.A, function() {})
```