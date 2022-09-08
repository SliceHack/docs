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

Thats crazy, right? You can now add events to your module with just 1 function!