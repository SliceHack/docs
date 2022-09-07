---
sidebar_position: 2
---

# Add Events to your Module

You can use functions to add events to your module. These functions are called when the event happens in minecraft.

```js
function onEnable() {
    // This function is called when the module is enabled
}

function onDisable() {
    // This function is called when the module is disabled
}

function init() {
    // This function is called when the module is initialized
}

function onUpdate(e) {
    // This function is called every update event
}

function onEvent3D(e) {
    // This function is called every 3D event
}

function onEventAttack(e) {
    // This function is called every attack event
}

function onEventChat(e) {
    // This function is called every chat event
}

function onEventChatMessage(e) {
    // This function is called every chat message event
}

function onEventClientBrand(e) {
    // This function is called when the client brand is changed
}

function onEventClientTick(e) {
    // This function is called every client tick event
}

function onEventEntityRender(e) {
    // This function is called every entity render event
}

function onEventJump(e) {
    // This function is called every jump event
}

function onEventKey(e) {
    // This function is called every key event
}

function onEventMouse(e) {
    // This function is called every mouse event
}

function onEventPacket(e) {
    // This function is called every packet event
}

function onEventPlayerReach(e) {
    // This function is called every player reach event
}

function onEventSafeWalk(e) {
    // This function is called every safe walk event
}

function onEventSlowDown(e) {
    // This function is called every slow down event
}

function onEvent2D(e) {
    // This function is called every 2D event
}


```

Thats crazy, right? You can now add events to your module with just 1 function!