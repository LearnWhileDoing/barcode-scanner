# State management

In the broadest possible sense, the state of an app is all of the information that the app is using and/or managing while running. This includes the app’s assets, all the variables that the Flutter framework keeps about the UI, animation state, textures, fonts, and so on. While this broadest possible definition of state is valid, it’s not very useful for architecting an app.

You don’t even manage some state that the Flutter framework handles those for you. So a more _useful_ definition of state is “whatever data you need in order to rebuild your UI at any moment in time”. Second, the state that you _do_ manage yourself can be separated into two conceptual types: _ephemeral_ state and _app_ state.

## Ephemeral state

Ephemeral state \(sometimes called _UI state_ or _local state_\) is the state you can neatly contain in a single widget.

This is an intentionally vague definition, so here are a few examples.

* current text inside a text field input
* current progress on a video
* current selected tab

Other parts of the widget tree seldom need to access this kind of state. There is no need to save and share it, and it doesn’t change in complex ways. In other words, there is no need to use state management techniques on this kind of state.

## App state

State that is not ephemeral, that you want to share across many parts of your app, and that you want to keep between user sessions, is what we call application state \(sometimes also called shared state\).

Examples of application state:

* User preferences
* Login info
* Notifications in a social networking app
* The shopping cart in an e-commerce app
* Read/unread state of articles in a news app

For managing app state, you’ll want to research your options. Your choice depends on the complexity and nature of your app, your team’s previous experience, and many other aspects. Much of the discussion of managing app state is outside of the scope of this tutorial, but we'll use some common patterns of managing app state in our final app.

## Managing state

![](../../.gitbook/assets/image%20%285%29.png)

There are different approaches for managing state. You, as the widget designer, choose which approach to use. For managing ephermeral state, there are a few common approaches to this:

* The widget manages its own state. For this approach, we would use a `StatefulWidget` that holds its own state \(as opposed to a `StatelessWidget`\). This approach is common when building simple forms like login forms, where the widget holds the information entered by the user.
* The parent widget manages the state of its children. This approach would make the parent widget a `StatefulWidget` while the children widgets are `StatelessWidget`s because they are not managing their own state. This is useful for more complex or multi-step forms.
* Sometimes it makes the most sense to use combine both of the previous approaches. If the children widget has simple ephemeral state that only it needs acccess to and the parent widget needs access to only some parts of the children widgets state \(for example to distribute the state to other widgets\), this would be the best approach. In this approach, all widgets would be `StatefulWidgets` because they hold their own state.

### **There is no clear-cut rule**

For example, you might decide that—in the context of your particular app—the selected tab in a bottom navigation bar is _not_ ephemeral state. You might need to change it from outside the widget or view, keep it between sessions, and so on. In that case, the current tab is active state.

There is no clear-cut, universal rule to distinguish whether a particular variable is ephemeral or app state. Sometimes, you’ll have to refactor one into another. For example, you’ll start with some clearly ephemeral state, but as your application grows in features, it might need to be moved to app state.

For those reasons, don't take the previous flow chart as an end-all-be-all. Follow this simple quote:

> “The rule of thumb is: [Do whatever is less awkward](https://github.com/reduxjs/redux/issues/1287#issuecomment-175351978).” — Dan Abramov



