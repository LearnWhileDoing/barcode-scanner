# Methods

Cars aren't considered very useful unless they can perform specific tasks. In Dart, these tasks are written as methods. We will make the following methods for our `Car` class: _beep_ and _drive_.

Go back to our `Car` class, and write the following method:

```java
class Car {
  /* instance variables... */

  public void beep() {
    System.out.println("BEEP");
  }
}
```

This can be written anywhere within the Car class, but methods are typically located underneath the constructor.

The `beep` method doesn't need to return anything back, so the `void` return type is used. Also, we want our Car to be able to be `beep`ed by the driver, so we must make it public to make it usable.

If we go back into our `Main.java` file, we can now call the beep method.

```java
myCar.beep();
```

In the console to the right, you should see **BEEP**. Your Car can now beep!

{% hint style="info" %}
You access methods on an object the same way you access instance variables using dot notation.
{% endhint %}

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

## Methods vs. Functions

What the difference between methods and functions? Well, that's kind of a trick questions, because they are basically the same thing!

**Methods are functions that belong to a class, like how instance variables are variables that belong to a class.**

