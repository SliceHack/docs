---
sidebar_position: 2
---

# Add Events to your Module

You can use `script.on` to add events to your module

# Init

this event is called when the module is initialized

```js
script.on('init', function (){});
```

# Enable

this event is called when the module is enabled

```js
script.on('enable', function() {});
```

# Disable

this event is called when the module is disabled

```js
script.on('disable', function() {});
```

# Update

The update event is called every player update

- `e.getX()` - Get the x position of the event
- `e.getY()` - Get the y position of the event
- `e.getZ()` - Get the z position of the event
- `e.getYaw()` - Get the yaw of the event
- `e.getPitch()` - Get the pitch of the event
- `e.isOnGround()` - Get if the event is on the ground
- `e.isPre()` - Get if the event is pre
- `e.setX(float)` - Set the x position of the event
- `e.setY(float)` - Set the y position of the event
- `e.setZ(float)` - Set the z position of the event
- `e.setYaw(float)` - Set the yaw of the event
- `e.setPitch(float)` - Set the pitch of the event
- `e.setOnGround(boolean)` - Set if the event is on the ground

```js
script.on('update', function(e) {});
```

# 2d

The 2d event is called every minecraft ``particleTick`` update

- `e.getPartialTicks()` - Get the partial ticks of the event
- `e.getWidth()` - Get the width of the event
- `e.getHeight()` - Get the height of the event
- `e.getScaledResolution()` - Returns the ScaledResolution of the event
- `e.setPartialTicks(float)` - Set the partial ticks of the event
- `e.setWidth(float)` - Set the width of the event
- `e.setHeight(float)` - Set the height of the event
- `e.setScaledResolution(ScaledResolution)` - Set the ScaledResolution of the event
```js
script.on('2d', function(e) {});
```

# 3d

the 3d event is called every minecraft entity render tick

- `e.getPartialTicks()` - Get the partial ticks of the event

```js
script.on('3d', function(e) {});
```

# attack

The attack event is called when a player attacks an entity

- `e.getEntity()` - Get the entity of the event
- `e.setEntity(Entity)` - Set the entity of the event

```js
script.on('attack', function(e) {});
```

# chat

this event is called when the player sends a chat message

- `e.getMessage()` - Get the message of the event
- `e.setMessage(String)` - Set the message of the event

```js
script.on('chat', function(e) {});
```

# clientBrand

this event is called when the client brand is received

- `e.getBrand()` - Get the brand of the event
- `e.setBrand(String)` - Set the brand of the event

```js
script.on('clientBrand', function(e) {});
```

# tick

this event is called every minecraft tick

```js
script.on('tick', function() {});
```

# entityRender

this event is called every minecraft entity render tick

- `e.getEntity()` - Get the entity of the event
- `e.getPartialTicks()` - Get the partial ticks of the event
- `e.isPre()` - Get if the event is pre
- `e.setEntity(Entity)` - Set the entity of the event
- `e.setPartialTicks(float)` - Set the partial ticks of the event

```js
script.on('entityRender', function(e) {});
```

# guiRender

this event is called when a gui should be rendered

- `e.getSr()` - Get the ScaledResolution of the event
- `e.getWidth()` - Get the width of the event
- `e.getHeight()` - Get the height of the event
- `e.getPartialTicks()` - Get the partial ticks of the event
- `e.setSr(ScaledResolution)` - Set the ScaledResolution of the event
- `e.setWidth(float)` - Set the width of the event
- `e.setHeight(float)` - Set the height of the event
- `e.setPartialTicks(float)` - Set the partial ticks of the event

```js
script.on('guiRender', function(e) {});
```

# jump

called when `player.jump()` is called

```js
script.on('jump', function() {});
```

# key

called when a key is pressed

- `e.getKey()` - Get the key of the event
- `e.setKey(int)` - Set the key of the event

```js
script.on('key', function(e) {});
```

# mouse

called when a mouse button is pressed

- `e.getButton()` - Get the button of the event
- `e.setButton(int)` - Set the button of the event

```js
script.on('mouse', function(e) {});
```

# packet

called when a packet is received or sent

- `e.getPacket()` - Get the packet of the event
- `e.isIncoming()` - Get if the event is incoming
- `e.isOutgoing()` - Get if the event is outgoing
- `e.setPacket(Packet)` - Set the packet of the event

```js
script.on('packet', function(e) {});
```

# reach

called when the client has to check the reach of the player

- `e.getReach()` - Get the reach of the event
- `e.setReach(float)` - Set the reach of the event

```js
script.on('reach', function(e) {});
```

# renderEntityModel

called when a entity model is rendered

- `e.getRenderer()` - Get the renderer of the event
- `e.getPartialTicks()` - Get the partial ticks of the event
- `e.getMaxRenderDistance()` - Get the max render distance of the event
- `e.model` - the model of the event
- `e.entity` - the entity of the event
- `e.p_77036_2_` - the x position of the event
- `e.p_77036_3_` - the y position of the event
- `e.p_77036_4_` - the z position of the event
- `e.p_77036_5_` - the yaw of the event
- `e.p_77036_6_` - the pitch of the event
- `e.scaleFactor` - the scale factor of the event

```js
script.on('renderEntityModel', function(e) {});
```

# slowDown

called when the player is slowed down 
ex: blocking sword

```js
script.on('slowDown', function() {});
```

# updateLWJGL

called when the Light weight java game library is updated

```js
script.on('updateLWJGL', function() {});
```


That's crazy, right? You can now add events with just `script.on`