---
sidebar_position: 4
---

# Java.extend()

`Java.extend()` is a function in nashorn that allows you to use ``extends <class>`` in JavaScript.

first you create a `Java.type()` variable

```js
const MyJavaClass = Java.type("java.lang.Thread");
```

then you use `Java.extend()` to extend the class
to override a method you would do `method: function() { /* code */ }`
to create a constructor you would do `constructor: function() { /* code */ }`

```js
const MyJavaClassExtended = Java.extend(MyJavaClass, {
    constructor: function() {
        // code
    },
    run: function() {
        Chat.print("Hello World!");
    }
});
```

then you can create a new instance of the class

```js
const myJavaClassExtendedInstance = new MyJavaClassExtended();
```

and then you can call what you overrode

```js
myJavaClassExtendedInstance.run();
```