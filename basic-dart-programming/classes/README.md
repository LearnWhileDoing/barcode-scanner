---
description: The building blocks of your Dart (and Flutter) programs
---

# Classes

Dart is an "object oriented program", which means that everything in Dart is based around the concepts of _classes_ and _objects_. To further explain this, we are going to make our own Dart program and create a class.

Because classes are such a fundamental part of Dart and Flutter programs, it is important that you have a good understanding of how classes work and how to use them. For this reason, we have split the different topics of Dart classes up into different lessons.

## 

## Methods

Cars aren't considered very useful unless they can perform specific tasks. In Java, these tasks are written as methods. We will make the following methods for our Car class: _beep_ and _drive_.

Go back to our Car class, and write the following method:

```java
public void beep() {
  System.out.println("BEEP");
}
```

This can be written anywhere within the Car class, but methods are typically located underneath the constructor.

The `beep` method doesn't need to return anything back, so the `void` return type is used. Also, we want our Car to be able to be `beep`ed by the driver, so we must make it public to make it usable.

If we go back into our `Main.java` file, we can now call the beep method.

```java
myCar.beep();
```

In the console to the right, you should see **BEEP**. Your Car can now beep!

We can write the same method but with a different method name and a different `println` argument for the `drive` method like so:

```java
public void drive() {
  System.out.println("I am driving");
}
```

Now we can go back to the `Main.java` file and call the `drive` method as well.

```text
myCar.drive();
```

## Recap

We now have written a Car class that has instance variables for its specific qualities, and has methods that allow it to perform specific tasks. Nice work!

### Challenge

Can you write your own class, in a new file called `House.java`, that represents a House? Use instance variables like color, town, rooms, or any others that you can think of!

