---
description: 'Peek-a-boo, I see you!'
---

# Scope

In most programming languages, a concept called _scope_ limits how your program has access to different variables and sometimes methods. Let's look at [the following example](https://dartpad.dev/e3714f7b3e5523408689c1d2a32a1ea1):

```java
// you can run this code in your browser:
// https://dartpad.dev/e3714f7b3e5523408689c1d2a32a1ea1

// please don't use this tutorial as baking advice :)

void prepareIngredients() {
    double sugar = 1;
    double butter = 0.5;
    double eggs = 2;
    double flour = 1.5;
}

double mix() {
}

void bake(double mixture) {
    /* bake a cake */
}
```

In this code example, we are simulating baking a cake. We have all of the ingredients prepared, so now we need to mix the ingredients. Simple, right?

```java
// you can run this code in your browser:
// https://dartpad.dev/0c9d616541cddda5a8e41e8de36faf09

double mix() {
    return sugar + butter + eggs + flour;
}
```

Well, not quite. This code will give us an error. Why? The ingredient variables are _out of scope_. This means that the ingredient variables are _scoped_ to the `prepareIngredients()` method, and are hidden and unavailable to the `mix()` method. How can we fix this? 

We can instead use _global_ variables. Global variables are available globally, or available everywhere in your project. Let's rewrite the cake recipe example, this time using global variables.

```java
// you can run this code in your browser:
// https://dartpad.dev/729983f6c10e5343c15779f20844ffa3

double sugar;
double butter;
double eggs;
double flour;

void prepareIngredients() {
    sugar = 1;
    butter = 0.5;
    eggs = 2;
    flour = 1.5;
}

double mix() {
    return sugar + butter + eggs + flour;
}

void bake(double mixture) {
    /* bake a cake */
}
```

Great! We now can use the variables anywhere within this class because it is _in scope_.

