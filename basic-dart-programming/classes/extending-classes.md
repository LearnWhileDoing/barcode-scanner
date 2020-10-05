---
description: The apple doesn't fall far from the tree!
---

# Extending classes

Suppose we are early mathematicians, and we know shapes exist. We can represent this with a class,  `Shape`. It has a name and a color. Right now, we don't know any shapes nor their own properties, but we know they exist.

```java
class Shape {
    String name;
    String color;

    Shape({ this.name, this.color });
}
```

Later on, we discover a shape known as a `Rectangle`. Its name is "Rectangle", it has its own color, but it also has a `width` and a `height`. A rectangle _**is-a**_ shape, so we will _inherit_ the `Shape` class.

We do this by using the keyword `extends`.

```java
class Rectangle extends Shape {
    int width;
    int height;
    
    Rectangle({ this.width, this.height, String color }) :
        super(name: "rectangle", color: color);
}
```

This constructor takes three parameters. The first two are assigned to the instance because of the `this` keyword, and the last one is a regular parameter.

After we made our parameterized constructor, you'll notice that there is a colon \(`:`\) followed by the _super_ keyword. What does that do?

### `super`

When you inherit a class, you are _extending_ it. That's why we use the keyword `extends`. However, we mustn't forget that the class we are creating, called the _sub_-class, has a parent class, called the _super_-class. The super-class has a constructor that must be called within the constructor of the sub-class. To do so, we use the `super` constructor. This calls the constructor of the parent class with the provided parameters.

In this case, the `super` constructor is the constructor of the `Shape` class. It takes two named parameters, as shown in the example. The name of the shape will always be "rectangle", and the color of the shape comes from the `color` parameter from the `Rectangle` constructor.

{% hint style="info" %}
A `Rectangle` _**is-a**_ `Shape`. Therefore, we extended the `Shape` class and inherit its properties.
{% endhint %}

