---
sidebar_position: 2
---

# Movement Utility

There are quite a few things in the `MoveUtil` class that you can use to make easier movement scripts.

## Jump

this function will set the player's motionY to 0.42 just like in Minecraft.

```js
MoveUtil.jump();
```

## Strafe (Mostly used for setting the speed of the player)

This function will add strafe to the player's motionX and motionZ.

```js
// Just set Strafe to players speed
MoveUtil.strafe();

// Set Strafe to a value
MoveUtil.strafe(0.5);
```

## Get Speed

This function will return the speed of the player.

```js
MoveUtil.getSpeed();
```

## Is Collided

This function will return if the player is collied or not.
    
```js
MoveUtil.isCollided();
```

## Get Blocks per Second

This function will return the blocks per second of the player.

```js
MoveUtil.getBPS();
```

## Reset motion

This function will set the motionX to 0, if the resetY boolean is true (motionY to 0), and motionZ to 0.

```js
// the parameter resets the motionY on the player
MoveUtil.resetMotion(true);
```

## Stop Movement

this function will disable all keybindings that are used for movement.

```js
MoveUtil.stop();
```



