---
description: Peek-a-boo
---

# Access specification

When creating the `Car` class, we made 4 instance variables. Each of these instance variables are _public_,  meaning it can be used anywhere the class is used.

```java
String make;
String model;
String color;
int year;
```

 We can also make them _private_ by adding an underscore \(`_`\) before the variable name. If it is _private_, then it can only be used **within** the class itself.

```java
String _make;
String _model;
String _color;
int _year;
```

Why would we want to make an instance variable private? Sometimes, we won't want the client of the class to be able to change or modify the value of an instance variable.

This grouping of information is known as encapsulation, and is one of the primary laws of OOP. This principle also applies to [methods](methods.md).

