---
description: How we perform specific tasks
---

# Functions

A function, or method, is a set of commands that run when we _call_ it. Like everything else in Dart, a Function is an object with the object type `Function`.

## Why use functions?

Functions are run whenever they are called. That means that they can be called as many times as needed. Functions are often used in order to re-use code, and to separate your code into different sub-tasks to make it easier to read and understand. 

If you have your program divided up into functions that each perform a specific task, it will be more legible than a program that has all of its code under a single function.

## Implementing a function

Here is an example of how we would _implement_, or code, a function.

```dart
String greet(String to, String from) { // function header
  var result = '$from says hello to $to!';
  return result; // return statement
}
```

This function `greet()` asks for the name of the greeter, and the recipient of the greeting. The function will _return_ a greeting. Let's deconstruct the _implementation_ to see what each part of the code does.

### Parameters

In the _function header_, we can see that the function asks for two _parameters_, `to` and `from`. It also shows that both of these parameters are Strings. There are multiple ways a function can accept parameters.

#### Positional Parameters

In the `greet()` function example, the two parameters are positional. This means that the position of the parameters determines how they are passed to the function. Consider the following example:

```dart
String to = "Martin";
String from = "Susan";
greet(to, from); // Susan says hello to Martin!
```

In this example, the `to` variable is passed to the `to` parameter because it is the first parameter passed, and the `from` variable is passed to the `from` parameter because it is the second parameter passed. However, if this was flip-flopped...

```dart
String to = "Martin";
String from = "Susan";
greet(from, to); // Martin says hello to Susan!
```

...the `from` variable is passed to the `to` parameter because it is the first parameter passed, and the `to` variable is passed to the `from` parameter because it is the second parameter passed.

{% hint style="info" %}
All positional parameters are required.
{% endhint %}

#### Named parameters

In Dart, you have the option of _naming_ parameters. This means that the position of the parameters does not matter, but you must specify which value is being passed to which parameter. For example, we can re-write the `greet()` function with named parameters:

```dart
String greet({String to, String from}) { // function header
  var result = '$from says hello to $to!';
  return result; // return statement
}
```

As you can see, not much changed, except we added brackets \(`{` and `}`\) around the parameters. However, what really changes is how we use the functions.

```dart
greet(to: "Martin", from: "Susan");
greet(from: "Susan", to: "Martin");
```

The only thing that matters when using named parameters is the name, rather than the position.

**By default, all named parameters are optional**. However, you can add a default value to the parameter so that your code runs less unpredictably.

```dart
String greet({String to = "someone", String from = "someone"})
// Now, the to and from parameters will default to "someone"

greet(to: "Martin"); // someone says hello to Martin!
greet(from: "Susan"); // Susan says hello to someone!
```

### Returning a value

When a function _returns_ a value, it means it gives back a value to wherever it is called. In the `greet()` function, a String is returned. How do we use that String value?

```text
String greeting = greet("Martin", "Susan");
```

The value that is returned from the `greet()` function will be given to the `greeting` variable. The `greeting` variable is assigned the value _returned_ by the `greet()` method.

