---
sidebar_position: 3
---

# Render

There are a few things in the `RenderUtil` class that you can use to make easier render scripts.

## Draw Image

This function will draw an image that is found in the class path

```js
/* this is function was made a while ago, 
    and we don't use it anymore because of HTML rendering */
RenderUtil.drawImage("something/texture.png", x, y, width, height);
```

## drawRoundedRect

this function will draw a rounded rectangle

```js
RenderUtil.drawRoundedRect(left, top, right, bottom, radius, color);
```

## drawHead

this function was used by our old TargetHUD, before we had HTML rendering

```js
RenderUtil.drawHead(uuid, x, y, width, height);
```


## drawRect

This function calls the `drawRect` function in the `Gui` class
But makes it easier to use.

```js
RenderUtil.drawRect(x, y, width, height, color);
```


## glColor

This function uses `Gl11.glColor4f` to set the color of the next render.

```js
/* you can either do an object 
    of a Color from java.awt or just do a value that returns from .getRGB() */
RenderUtil.glColor(hex);

const Color = Java.type("java.awt.Color");
RenderUtil.glColor(new Color(255, 255, 255));
```