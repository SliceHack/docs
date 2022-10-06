---
sidebar_position: 5
---

# Rotation

there are a couple of things in the `RotationUtil` class that you can use to make easier scripts.

## getDirection

this function will return the direction off the player as a double based of the yaw. although
this function is mostly used for the `MoveUtil.strafe` function.

```js
RotationUtil.getDirection();
```

## isInFov

this function will return a boolean if an entity is in the field of view of the player.

```js
// fov can be any number through 0-360
RotationUtil.isInFov(entity, fov);
```