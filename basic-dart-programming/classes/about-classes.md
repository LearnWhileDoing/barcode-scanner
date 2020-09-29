# About classes

Congrats! You just created an _instance_, or an _object_, of the Car class!

Let's look at the variable declaration. 

```java
Car myCar = new Car();
```

We can see that the variable `myCar` is declared with the data type `Car`. This tells Dart that this variable will be an object of the class Car.

{% hint style="info" %}
The `new` keyword is optional. You can create a new instance of a class without it.
{% endhint %}

In the next example, we tell Java that the variable `myHouse` will be of the data type `House`. We haven't made the `House` class so this code won't work, but go ahead and try to make your own House class after this lesson!

```java
House myHouse = new House();
```

In the variables lesson, we learned about the primitive data types in Dart, and you will notice that neither `Car` nor `House` are any of those. That is because `Car` and `House` are classes, and are considered _non-primitive_. If you haven't noticed, type `String` is a class, and is therefore _non-primitive_ as well.

When we create an instance of a class, we tell Dart to create a _new_ object. If we want a new car, we would write `new Car()`.

{% hint style="info" %}
Remember that **classes represent things or objects, as well as abstract things**. Things like motors, cars, clothing items, are things that can be represented as classes. Also, abstract things like errors, colors, or even Strings can be represented as classes.

In short, **classes should represent anything that there can theoretically be multiple "instances" of**.
{% endhint %}

