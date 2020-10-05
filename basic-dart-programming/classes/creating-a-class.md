# Creating a class

We are going to _implement_ the `Car` class now. The class will represent an actual car.

## Class Header

Whenever you create a new class, you will begin with the following line. Of course, you will change `MyClass` to whatever classname you need.

```java
class Car {
```

This line is called the _class header_, and it is used to tell Dart what your class is called, as well as which class you plan on [inheriting](../../untitled.md)[ and extending](../../untitled.md) and/or which interface you plan on [implementing](../../untitled.md).

{% hint style="info" %}
Typically, classes are titled in **PascalCase** as opposed to **lowercase**.
{% endhint %}

## Instance Variables

When we think about a car, what specific qualities belong to that car? Whatever makes a specific instance of a class unique is considered an _instance variable_, as it only belongs to one instance \(one object\) of the class.

In the case of a car, what comes to mind is the _make_, _model_, _color_, and _year_ of the car. The make, model, and color of the car are all `String` values, while the year should be an integer.

Let's make these instance variables. This will be inside the Car class.

```java
class Car {
  String make;
  String model;
  String color;
  int year;
}
```

## Constructor

Great, now our car has specific attributes that make it unique. However, there is no way to create an object with unique properties yet. As you can see, these instance variables don't have any values assigned to them.

To do this, we will write a class _constructor_. The constructor of a class is a special method \(with no return type\) called whenever a new instance of a class is created. Usually, we use constructors to assign values to our instance variables. This is what our constructor should look like inside the Car class.

```java
class Car {
  public String make;
  public String model;
  public String color;
  public int year;

  Car();
}
```

But wait, those instance variables still were never assigned a value! How do we fix that?

Constructors can accept parameters like functions. They can be named or positional. For this example, we will make them named.

```java
Car({ this.make, this.model, this.color, this.year });
```

This is called a _parameterized constructor_ because it now has different _parameters_. We can use these parameters to assign values to the instance variables.

{% hint style="info" %}
The `this` keyword simply tells Dart to assign the instance variable to _this_ instance.
{% endhint %}

Now, we can update the `main()` method to create a `new Car`.

```java
void main() {
    Car myCar = new Car(
        make: "Porsche", 
        model: "Taycan", 
        color: "blue", 
        year: 2020
    );
}
```

After adding the arguments to the variable declaration, we now have a blue 2020 Porsche Taycan stored as the variable `myCar`. Nice!

