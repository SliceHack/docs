---
sidebar_position: 2
---

# Implement Minecraft Instance

You can use the `mc` variable in the project to access the Minecraft instance

```js
const name = "AutoJump";
const description = "Will Automatically Jump when you are onGround";
const category = MOVEMENT;

function onUpdate() {
    if(mc.thePlayer.onGround) return;
    if(mc.thePlayer.isCollidedVertically) return;
    mc.thePlayer.jump();
}
```

That's crazy right you can access the Minecraft instance in JavaScript!