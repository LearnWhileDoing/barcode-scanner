---
description: Referring to an instance variable or method
---

# Accessing object properties

When we made the `Car` class, we gave it multiple instance variables that described what the car looked like. They were:

* `String make`
* `String model`
* `String color`
* `int year`

All of these instance variables are public, which means that we can access them from anywhere \(if they were private, we wouldn't be able to access them from outside the class\). But how do we access the instance variables inside of an object? To do that, we use _dot notation_ \(`.`\).

In the following example, we have our blue 2020 Porsche Taycan.

```dart
void main() {
    Car myCar = new Car(
        make: "Porsche", 
        model: "Taycan", 
        color: "blue", 
        year: 2020
    );
}
```

Let's say that when we made the `Car`, we didn't know what it's color is.  However, we do have access to the `myCar` object, with all of its instance variables. We can _refer_ to \(access\) these properties with a dot, followed by the name of the instance variable like so:

```dart
String color = myCar.color;
```

Now, the variable `color` will be assigned to the value of the color of `myCar`.

