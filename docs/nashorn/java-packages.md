---
sidebar_position: 2
---

# Packages

``Packages`` is a global object that allows you to get static ``methods``/```fields``` in a Java Class

```js
const System = Packages.java.lang.System; // access the Java System class
System.out.println("Hello World!"); // print "Hello World!" to the console
```

That's crazy right all you need to do to access a Java class is to use ``Packages`` and then the full path to the class.