---
layout: post
title: "Flutter weekly - Stack Widget flutter"
meta: "flutter weekly stack widget flutter"
categories: "flutter"
tags: flutter dart flutter-weekly
---

![Flutter - Flutter weekly Stack and Postioned Widget][flutter]

If you are wondering [What is flutter](https://sapidlabs.com/flutter/2019/08/12/what-is-flutter.html), you might wanna checkout our 2 minute [Introduction to Flutter](https://sapidlabs.com/flutter/2019/08/12/what-is-flutter.html) post. Since Everything in flutter is a Widget. It is good to have a basic understanding of what a particular widget does. We will be picking up one widget per weekly to explain about it in brief about it. Stay Tuned!


### What is Stack in flutter?

[Stack](https://api.flutter.dev/flutter/widgets/Stack-class.html) is another widget provided by flutter that positions its child widgets relative to edge of the example. Doesn't ring any bell?? We will cover with example.

Stack can have two types of child widgets within them. These are [Positioned](https://api.flutter.dev/flutter/widgets/Positioned-class.html) and Non-positioned widgets.

Postioned - Those which are wrapped within Positioned widget, something like the following:

```dart
Positioned(
  child: Container(
    ...
  )
)
```

Stack takes children as argument, which is list of elements that will be part of the stack. The elements are placed on the screen starting from the first child being at the bottom to the last child at the top and is left to right in alignment.

The following code will draw three containers on the mobile screen, with green, red and blue containers respectively.

```dart
...
Stack(
  children: <Widget>[
    Container(
      width: 100,
      height: 100,
      color: Colors.green[300],
      child: Text(
        'Green',
        style: TextStyle(
          color: Colors.white,
          fontSize: 20
        ),
      ),
    ),
    Container(
      width: 90,
      height: 90,
      color: Colors.red[400],
      child: Text(
        'Red',
        style: TextStyle(color: Colors.white, fontSize: 20),
      ),
    ),
    Container(
      width: 80,
      height: 80,
      color: Colors.indigo[300],
      child: Text(
        'Blue',
        style: TextStyle(color: Colors.white, fontSize: 20),
      ),
    ),
  ],
),
...
```

## TODO: ADD IMAGE HERE

As you can see in the example, that the Green was provided as the first child so it is bottom most amoung the three containers and Blue being at the top.

## TODO : ADD LINK
Next tutorial is [How to use Positioned Widget with Stack?]() (2 min read.)

[flutter]: /assets/images/shared/flutter-sapidlabs.jpg
