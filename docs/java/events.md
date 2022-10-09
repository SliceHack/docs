---
sidebar_position: 3
---

## Events

Events are a way to listen for certain actions in the game.

### Events 

# EventUpdate

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

```java
@EventInfo
public void onUpdate(EventUpdate e) {
    // do stuff
}
```

# Event2D

The 2d event is called every minecraft ``particleTick`` update

- `e.getPartialTicks()` - Get the partial ticks of the event
- `e.getWidth()` - Get the width of the event
- `e.getHeight()` - Get the height of the event
- `e.getScaledResolution()` - Returns the ScaledResolution of the event
- `e.setPartialTicks(float)` - Set the partial ticks of the event
- `e.setWidth(float)` - Set the width of the event
- `e.setHeight(float)` - Set the height of the event
- `e.setScaledResolution(ScaledResolution)` - Set the ScaledResolution of the event

```java
@EventInfo
public void onRender2D(Event2D e) {
    // do stuff
}
```

# Event3D

the 3d event is called every minecraft entity render tick

- `e.getPartialTicks()` - Get the partial ticks of the event

```java
@EventInfo
public void onRender3D(Event3D e) {
    // do stuff
}
```

# EventAttack

The attack event is called when a player attacks an entity

- `e.getEntity()` - Get the entity of the event
- `e.setEntity(Entity)` - Set the entity of the event

```java
@EventInfo
public void onRender3D(EventAttack e) {
    // do stuff
}
```

# EventChat

this event is called when the player sends a chat message

- `e.getMessage()` - Get the message of the event
- `e.setMessage(String)` - Set the message of the event

```java
@EventInfo
public void onChat(EventChat e) {
    // do stuff
}
```

# EventClientBrand

this event is called when the client brand is received

- `e.getBrand()` - Get the brand of the event
- `e.setBrand(String)` - Set the brand of the event

```java
@EventInfo
public void onBrand(EventClientBrand e) {
    // do stuff
}
```

# EventTick

this event is called every minecraft tick

```java
@EventInfo
public void onTick(EventTick e) {
    // do stuff
}
```

# EventEntityRender

this event is called every minecraft entity render tick

- `e.getEntity()` - Get the entity of the event
- `e.getPartialTicks()` - Get the partial ticks of the event
- `e.isPre()` - Get if the event is pre
- `e.setEntity(Entity)` - Set the entity of the event
- `e.setPartialTicks(float)` - Set the partial ticks of the event

```java
@EventInfo
public void onEntityRender(EventEntityRender e) {
    // do stuff
}
```

# EventGuiRender

this event is called when a gui should be rendered

- `e.getSr()` - Get the ScaledResolution of the event
- `e.getWidth()` - Get the width of the event
- `e.getHeight()` - Get the height of the event
- `e.getPartialTicks()` - Get the partial ticks of the event
- `e.setSr(ScaledResolution)` - Set the ScaledResolution of the event
- `e.setWidth(float)` - Set the width of the event
- `e.setHeight(float)` - Set the height of the event
- `e.setPartialTicks(float)` - Set the partial ticks of the event

```java
@EventInfo
public void onEventShouldGuiRender(EventGuiRender e) {
    // do stuff
}
```

# EventJump

called when `player.jump()` is called

```java
@EventInfo
public void onJump(EventJump e) {
    // do stuff
}
```

# EventKey

called when a key is pressed

- `e.getKey()` - Get the key of the event
- `e.setKey(int)` - Set the key of the event

```java
@EventInfo
public void onKeyPress(EventKey e) {
    // do stuff
}
```

# EventMouse

called when a mouse button is pressed

- `e.getButton()` - Get the button of the event
- `e.setButton(int)` - Set the button of the event

```java
@EventInfo
public void onMousePress(EventMouse e) {
    // do stuff
}
```

# EventPacket

called when a packet is received or sent

- `e.getPacket()` - Get the packet of the event
- `e.isIncoming()` - Get if the event is incoming
- `e.isOutgoing()` - Get if the event is outgoing
- `e.setPacket(Packet)` - Set the packet of the event

```java
@EventInfo
public void onEventPacket(EventMouse e) {
    // do stuff
}
```

# EventReach

called when the client has to check the reach of the player

- `e.getReach()` - Get the reach of the event
- `e.setReach(float)` - Set the reach of the event

```java
@EventInfo
public void onReach(EventReach e) {
    // do stuff
}
```

# EventRenderEntityModel

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

```java
@EventInfo
public void onModelRender(EventRenderEntityModel e) {
    // do stuff
}
```

# EventSlowDown

called when the player is slowed down
ex: blocking sword

```java
@EventInfo
public void onSlowdown(EventSlowDown e) {
    // do stuff
}
```

# EventUpdateLWJGL

called when the Lightweight java game library is updated

```java
@EventInfo
public void onLWJGLUpdate(EventUpdateLWJGL e) {
    // do stuff
}
```

### Registering an event

You can skip this part if you are creating a module

the first parameter is the object to search for methods with the `@EventInfo` annotation

```java
Slice.INSTANCE.getEventManager().register(new MyListener());
````
