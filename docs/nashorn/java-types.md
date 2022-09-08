---
sidebar_position: 2
---

# Java.type()

You can use `Java.type()` to get a java class. This is useful for registering new Objects that are not in `JavaScript`

```js
/* Java.type() is a function that allows you to create  
    new instances of java classes */
const ArrayList = Java.type("java.util.ArrayList");
const list = new ArrayList(); // create a new ArrayList instance
```

That's crazy right all you need to do to create a new instance of a Java class is to use `Java.type()` and then the full path to the class.