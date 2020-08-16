---
description: What does a Dart program look like?
---

# Program Structure

_The code and explanations used in this section is borrowed from and inspired by the_ [_Dart language tour_](https://dart.dev/guides/language/language-tour)_._

## Basic Dart program

Let's look at a basic Dart program to understand more about the Dart programming language.

```dart
// Define a function.
String displayInteger(int aNumber) {
  return "The number is $aNumber."; // Return a String.
}

// This is where the app starts executing.
void main() {
  var number = 42; // Declare and initialize a variable.
  String text = displayInteger(number); // Call a function.
  print(text); // Print to console.
}
```

You can run this program on DartPad at [https://dartpad.dev/78de3f702019482ba30def50706cbbe6](https://dartpad.dev/78de3f702019482ba30def50706cbbe6).

This program will print `The number is 42` to the console. In every Dart program, there are key parts to the language that you will notice.

### Dart-specific syntax

Notice how each block of code begins and ends with _curly braces_. This is evident in the methods `displayInteger` and `main`. Curly braces show Dart what part of your program belongs with which block of code.

Also, each _code statement_ must end with a semicolon.

### Comments

When we write programs in any language, we want to be able to understand what specific parts of our code does. We can write _comments_ in our code to give ourselves and other people an idea of what this code does.

There are two ways of writing comments in Dart:

```java
/**
 * multi-line comment
 */

// single line comment
```

Multi-line comments must start with `/*` and end with `*/`

### Methods

Methods, or functions, are a set of commands that are used perform specific actions. We declare two _top-level_ methods, `displayInteger` and `main`. Top-level methods are globally available, meaning that they can be used anywhere in your program. **The `main` method is the** _**entry-point**_ **of all Dart programs.** Methods help us to be able to reuse code, so that we can write it once and then call it again anywhere else in our code.

You might notice that we never declare the `print` method, so how are we able to use it? The `print` method is provided to us by the Dart language itself, so it is available even though we didn't define what it does. The `print` method prints data to the console that is running the program.

### Data Types

In this program, you will notice the usage of `void` and `String`. These are Dart _data types_, and they tell Dart what type of data a specific value will be. In this case, stating `void` before a method tells Dart not to expect a value to be returned from this method \(this is a _return type_\), and stating `String` will tell Dart that this method should return a `String`.

Learn more about data types in the [variables lesson]().

### `var` keyword

In most programming languages, you can declare _variables_ and assign values to them. Many _statically-typed_ languages like Java do not let you change the data type of a variable in the middle of a program; Dart is dynamically typed, which means that the type of a variable can be changed. This can be done with the `var` keyword \(used for variables\) or the `dynamic` keyword \(in all other cases\).

