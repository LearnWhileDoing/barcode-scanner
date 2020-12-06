---
description: Using declarative programming with Flutter
---

# Flutter "declaritivity"

## State in Flutter

When working with widgets in Flutter, almost everything you code will be declarative. Your app with reflect the current _state_ of your app.

What is _state_? Not like a state of a country. State is "the particular condition that someone or something is in at a specific time." In apps, the _state_ of your app is the current data and information that is present in your app. For example, if you are on the home page, the state of your app is on the home page. If you navigate to the settings page, you change the state to the navigation page.

Your app will probably be more complex than having blank home and settings pages: you will most likely have buttons, text fields, switches, etc. All of those have their own individual states: buttons have pressed and unpressed states, switches have on and off states, and text fields have the state of whatever is typed into them.

### Tying in declarative programming

Below is a function that represents how Flutter works. You learned in the Dart Fundamentals course \(or in math class!\) that a function takes an input and returns an output. Note that the following is a symbolic representation of how Flutter works. 

* In Flutter, your app consists of a build method that puts all of your widgets together. This is the _function_ of your app.
* Then, the state of your app is inputted into the function of your app.
* The result of the function is the UI that is displayed to your user.

![](https://flutter.dev/assets/development/data-and-backend/state-mgmt/ui-equals-function-of-state-54b01b000694caf9da439bd3f774ef22b00e92a62d3b2ade4f2e95c8555b8ca7.png)

> A mathematical formula of UI = f\(state\). 'UI' is the layout on the screen. 'f' is your build methods. 'state' is the application state.

Typically, whenever the state of your app is changed, Flutter "rebuilds" your app. The function runs again, and the UI is updated.

This is majorly different from imperative programming. With declarative programming, your application can be represented as a single function of state, whereas with imperative programming this is not as simple to do.

