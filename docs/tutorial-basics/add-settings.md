---
sidebar_position: 2
---

# Add Settings to your Module

You can put these anywhere inside the module I just don't recommend putting them in the event functions.

## Boolean Value

- `getValue()` - Returns the value of the setting
- `setValue(value)` - Sets the value of the setting

```js
// name (the name of the setting), value (the boolean value of the setting)
const boolean = script.registerBoolean("Boolean", true);
```

## Mode Value

- `getValue()` - Returns the value of the setting
- `getValues()` - Returns all values of the array
- `setValue(value)` - Sets the value of the setting
- `cycle()` - Cycles the value of the setting
- `cycleBackwards()` - Cycles the value of the setting in reverse
```js
// (name of the setting) name, (the modes) ...modes
const mode = script.registerMode("Mode", "1", "2", "3", ...etc);
```

## Number Value

- `getValue()` - Returns the value of the setting
- `getMin()` - Returns the minimum value of the setting
- `getMax()` - Returns the maximum value of the setting
- `getType()` - Returns the type of the setting
- `setValue(value)` - Sets the value of the setting
- `setMin(value)` - Sets the minimum value of the setting
- `setMax(value)` - Sets the maximum value of the setting
- `setType(type)` - Sets the type of the setting
```js
// (name of the setting) name, (min) min, (max) max, (the defualt value) value, (FLOAT, DOUBLE, INTEGER, LONG) type
const number = script.registerNumber("Number", 0, 10, 5, FLOAT);
```

That's crazy right you can register a setting with one line!