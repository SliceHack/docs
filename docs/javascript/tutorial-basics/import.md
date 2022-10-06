---
sidebar_position: 5
---

# Import

The `import` statement is a more simplified way to import classes without having to use the `Java.type` function.

```js
import Minecraft from 'net.minecraft.client.Minecraft';
```

This is the same as:

```js
const Minecraft = Java.type('net.minecraft.client.Minecraft');
```

You can also just ``import()`` so you won't have to assign it to a variable:

```js
import('net.minecraft.client.Minecraft').getMinecraft();
```

This is the same as:

```js
Java.type('net.minecraft.client.Minecraft').getMinecraft();
```