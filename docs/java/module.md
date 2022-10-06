---
sidebar_position: 2
---

## Create a Module

First you create a new class extending `slice.module.Module` and add the`@ModuleInfo` annotation.

## ModuleInfo

The `@ModuleInfo` annotation requires a `name` field and `category` field.
you can also add a `description` field to give a description of the module.

The `name` field is the name of the module.
The `description` field is the description of the module.
The `category` field is the category of the module.

# ModuleInfo Example

```java
@ModuleInfo(
    name = "Example Module",
    description = "This is an example module", 
    category = Category.MISC
)
public class SomeModule extends Module {}
```

## Module

The `Module` class is what you extend to create a module.

There are only 3 methods in the `Module` class that you can override. (without breaking the module)

`init()` is called when the module is initialized.

`onEnable()` is called when the module is enabled.

`onDisable()` is called when the module is disabled.

# Module Example

```java
    @Override
    public void init() {
        // Called when the module is initialized.
    }
    
    @Override
    public void onEnable() {
        // Called when the module is enabled.
    }
    
    @Override
    public void onDisable() {
        // Called when the module is disabled.
    }
```

## Events

To register events you make a method the `EventManager` can read and call.
with annotation on the method `@EventInfo` and the event as the parameter.

# Event example

```java
@EventInfo
public void onEvent(EventUpdate event) {
    // Called when the event is called.
}
```

## Register module

To register the module go back to your `Main` class and add on to `onStartup()` method.

```java
Slice.INSTANCE.getModuleManager().registerModule(new SomeModule());
```