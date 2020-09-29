---
description: How we store and save data in Dart
---

# Variables and Built-in Types

## What is a variable?

A _variable_ is a container that is used for storing values.

Consider this analogy: a variable is like a vocabulary notecard. One side of the notecard is used for the word, and the other side is used for definition of that word. Here is an example of that in practice. `int amount = 3;`

This line of code is called a _variable declaration_, and consists of a left and right-hand side.

* The left-hand side of a variable declaration has a data type \(`int`\) and a name \(`amount`\), in that order. This tells your computer that the variable `amount` has the data type `int`, which will never change.
* The right-hand side is the _value_ which the variable will store. In this case, the value will be 3.

{% hint style="info" %}
Values _can_ change, data types _cannot_.
{% endhint %}

## Data Types

In the above example, variable `amount` is the type `int`. What does that mean?

As the name suggests, different _data types_ specify what type of data can be assigned as the value to a variable. Dart is an OOP language, which means that every type of data is an _object_. In Dart,

### Built-in Data Types

8 different primitive data types are available in Java. They consist of:

1. **bool** - short for boolean; `true` or `false`
2. **int** - an integer value
3. **double** - a decimal value
4. **String** - a "string" of text
5. **List** - also known as an array; an ordered "list" of items
6. **Set** - an unordered List with no duplicates
7. **Map** - for key-value pairs

Notice how the first 3 data types are lowercase, while the rest are capitalized. This is how they are represented in Dart. For the most part, we will only be using the first 5 of these data types; we will go over the last two in the advanced section.

### Dynamic Data

Sometimes, you have data that isn't always a number or a String. In these cases, you have what is called "dynamic" data, and you will need the `dynamic` keyword.

For example, you will often take data from a user. This data can be provided as either a String or a number:

```dart
dynamic userData = "...";
// or...
dynamic userData = 123;
```

As you can see, when using the `dynamic` keyword, the value can be of any type.

## Quiz

{% tabs %}
{% tab title="Question" %}
How would you declare a variable `age`? _Hint: use the `int` data type_
{% endtab %}

{% tab title="Answer" %}
```dart
int age = 15;
```
{% endtab %}
{% endtabs %}

