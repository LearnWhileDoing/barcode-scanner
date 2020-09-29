---
description: Peek-a-boo
---

# Access specification

When creating the `Car` class, you may have noticed the `public` keyword before our instance variables.

```java
public String make;
public String model;
public String color;
public int year;
```

The first keyword, `public`, is the access specifier. This tells Java where this instance variable can be used. If tit is _public_,  it can be used anywhere the class is used. If it is _private_, then it can only be used **within** the class itself.

Why would we want to make an instance variable private? Sometimes, we won't want the client of the class to be able to change or modify the value of an instance variable.

This grouping of information is known as encapsulation, and is one of the primary laws of OOP. This principle also applies to [instance variables]().

