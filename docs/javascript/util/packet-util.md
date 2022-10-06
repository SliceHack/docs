---
sidebar_position: 2
---

# Packet

There are a few things you can do in the `PacketUtil` to help you with packets.

## sendPacket

This function will send a packet to the server with an event.

```js
const C03PacketPlayer = Java.type("net.minecraft.network.play.client.C03PacketPlayer");
PacketUtil.sendPacket(new C03PacketPlayer()); // the Flying packet in bukkit (for some reason)
```

## sendPacketNoEvent

This function will send a packet to the server without an event.
You basically do the same thing as `sendPacket` but you use `sendPacketNoEvent` instead.

```js
const C03PacketPlayer = Java.type("net.minecraft.network.play.client.C03PacketPlayer");
PacketUtil.sendPacketNoEvent(new C03PacketPlayer());
```

## isMovementPacket

This function will return if the packet is a movement packet or not.

```js
const C04PacketPlayerPosition = Java.type("net.minecraft.network.play.client.C03PacketPlayer.C04PacketPlayerPosition");
PacketUtil.isMovementPacket(new C04PacketPlayerPosition()); // returns a boolean
```