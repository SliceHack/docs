---
sidebar_position: 1
---

# Create a Module

To create a must create a file at `%Slice-Dir%/Scripts/<FileName>.js`

The next thing you want to do is right a `script.exports` for the script to understand

There are only 3 variables you can use in the `script.exports`

You can use `name` to set the name of the module

You can use `description` to set the description of the module (this is not required)

You can use `category` to set the category of the module

```js
script.exports = {
    name: "Test",
    description: "This is a test module",
    category: Category.Movement
};
```

## Category

The category is a enum that you can use to set the category of the module

```js
Category = {
    COMBAT: "Combat",
    MOVEMENT: "Movement",
    PLAYER: "Player",
    WORLD: "World",
    RENDER: "Render",
    MISC: "Misc",
};
```