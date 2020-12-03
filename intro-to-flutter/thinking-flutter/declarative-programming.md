---
description: The pattern and style of programming used in Flutter
---

# Declarative Programming

Take a look at two separate coding examples.

Example \#1:

```dart
var container = new Container();
var button = new Button();
button.setText("Click Me!");
button.onClick(() { print("clicked"); });
container.addChild(button);
```

Example \#2:

```dart
var container = new Container(
    children: [
        new Button(
            text: "Click Me!",
            onClick: () { print("clicked"); }
        )
    ]
)
```

You probably notice that these two examples look quite different from each other, but would you be surprised to know that, theoretically, these two examples of code could do the same things?

In this lesson, we'll take a look at two different programming _paradigms_, or the patterns and styles of programming that programmers use. We'll look at imperative programming and its shortcomings for app development, and then discuss why Flutter uses declarative programming and how it benefits us as app developers.

## Imperative Programming

Of the previous 2 examples, can you guess which is an example of imperative programming? If you guessed example \#2, you'd be wrong! Example \#1 is an example of the imperative programming paradigm.

With imperative programming, your entire codebase will look like a list of commands. Every part of your UI is controlled by a list of commands: that includes setting values and properties \(color, text, etc.\) and listening to events \(when the user clicks a button, when the user types, etc.\).

At first glance, it may appear that imperative programming is more intuitive, especially for beginners. However, there are are a couple of shortcomings for this programming style, especially when creating UIs:

* **It's very difficult to visualize the final layout of your app.** Your app will most likely have tons of widgets inside of widgets inside of widgets. With imperative programming, you won't be able to visualize that layered design of your app.
* **It becomes tedious to assign each property individually.** Say you have a Button widget. You want it to have a color, an icon, a text label, and you need to listen to when the user clicks the button. Imperative programming would require you to set each of these properties and listeners individually, instead of altogether.
* Once you become used to it, **declarative programming is far more intuitive**. Trust us :\)

## Declarative Programming

Example \#2 uses the declarative programming paradigm, and is very similar to what building widgets looks like in Flutter. In your code, each widget is _nested_ within its _parent_, like they are in your app. __That makes it much easier to visualize the layout of your app that it would be with imperative programming.

For app developers \(or anyone designing UIs\), declarative programming is actually much more intuitive for creating UIs. Additionally, the more you use it, the more comfortable you will feel with it.

Next, we'll learn about how declarative programming dictates how we program our apps.

