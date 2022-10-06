---
sidebar_position: 1
---

# How to load a jar file

The `script.json` is what slice will read from the jar classpath
to determine what to do with the project. It is a json file that

## Example

```json
{
  "main": "com.example.SomeClass"
}
```


# Main

The main class is what slice will use to initialize your project. with

class must extend `com.sliceclient.script.SliceScript`

will call Method `onEnable()` once the project is initialized.

will call Method `onDisable()` once the project is shutdown.

## Example

```java
package com.example;

import com.sliceclient.script.SliceScript;

public class SomeClass extends SliceScript {

    /**
     * Called when slice starts up.
     * */
    @Override
    public void onEnable() {
        System.out.println("Hello World!");
    }
    
    /**
     * Called when slice shuts down.
     * */
    @Override
    public void onDisable() {
        System.out.println("Goodbye World!");
    }
}
```