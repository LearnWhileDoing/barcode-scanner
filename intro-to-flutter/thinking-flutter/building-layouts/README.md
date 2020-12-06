# Composing layouts

When you start to design your app, you will have to take _layouts_ into consideration. Each view, also known as a page, of your app will have multiple layouts within layouts. Your app will probably be layed out with many nested layouts, which will be composed into a _tree_ similar to something like this:

![Flutter widget tree](../../../.gitbook/assets/image%20%281%29.png)

We will look at how once you have **visually** designed your app, you can **logically** design it using Flutter layout patterns.

## Layout patterns in Flutter

Let's revist the "everything is a widget" trope.

> The core of Flutter’s layout mechanism is widgets. In Flutter, almost everything is a widget—even layout models are widgets. The images, icons, and text that you see in a Flutter app are all widgets. But things you don’t see are also widgets, such as the rows, columns, and grids that arrange, constrain, and align the visible widgets.

Remember that, in Flutter, everything in your app's UI is a widget, or a composition of multiple widgets. Typically, if you want your app to look good at not just hastily thrown together, you will want to build layouts in Flutter that make your app look more polished. How do you build and compose layouts in Flutter?

### Choose a layout widget

In Flutter, there are [a lot of layout widgets](https://flutter.dev/docs/development/ui/widgets/layout) that you can use to compose layouts, each of which serve their own purpose. Take a look at the following examples that shows how you can use multiple layout widgets to compose layouts:

![](../../../.gitbook/assets/image%20%284%29.png)

You will choose your layout widget based on what your layout requires. We made a useful reference for the most common layout widgets in Flutter.

Some widgets \(like Container and Center\) help you to organize and style individual child widgets. Other widgets \(like Row and Column\) allow you to organize and align multiple widgets within a single widget.

### Single-child layout widgets

If you are using a single-child layout widget like Align, Center, or Container, you will pass a single child widget. This child widget is called the _visible_ widget.

### Multi-child layout widgets

When using multi-child layout widgets, you will pass an array of multiple visible widgets. It will become the parent to these children widgets.

{% tabs %}
{% tab title="Aligning children" %}
The most basic multi-child widgets are Column and Row. They help you to align children widgets vertically and horizontally, respectively. Both of these widgets have two _axes_, the main axis and cross axis.

![The main axis for Row is horizontal, while the cross axis is vertical.](../../../.gitbook/assets/image%20%282%29.png)

![The main axis for Column is vertical, while the cross axis is horizontal.](../../../.gitbook/assets/image%20%283%29.png)

Depending on how you choose to align your children widgets, they can either be at the top, middle, or bottom of the main and cross axes.
{% endtab %}

{% tab title="Packing children" %}
When using a multi-children layout widget, there are two ways to size each axis. You can have them either take up maximum space or minimum space. 

* When you choose for the axis to take up **maximum** space, it will take up as much space in its parent as it can in that direction. For example, if you set the main axis of a Column widget to take up maximum space, it will stretch out as much as it can in the veritcal direction.
* When you choose for the axis to take up **minimum** space, it will take up as little space as it can in that direction. This means that the widget will compress down to the size of its children.
{% endtab %}
{% endtabs %}

