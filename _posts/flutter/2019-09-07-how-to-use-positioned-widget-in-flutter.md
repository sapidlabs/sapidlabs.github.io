---
layout: post
title: "How to use positioned widget in flutter?"
meta: "sapidlabs positioned widget flutter"
categories: "flutter"
tags: flutter dart flutter-weekly
---

![Flutter - Stack and Postioned Widget][flutter]

This Recommends checking out our previous post on, the usage of [Stack widget](https://sapidlabs.com/flutter/2019/09/07/how-to-use-stack-widget-flutter.html)( 2 min read ). I am waiting....

Ok Done? So let's get started.

### How to use Postioned Widget in flutter

[Positioned Widget](https://api.flutter.dev/flutter/widgets/Positioned-class.html), As the name suggests It is something related to position of some widget. Right !! Positioned is a widget provided by flutter, that controls where a child of Stack is positioned.


So referring to our previous example, of a Stack with three colored container in it. Let's wrap them up into a `Positioned` widget.

The following code will draw three containers on the mobile screen, with green, red and indigo colored containers respectively.

```dart
...
Stack(
  children: <Widget>[
    Positioned(
      top: 20,
      left: 20,
      height: 200,
      width: 200,
      child: Container(
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
    ),
    Positioned(
      top: 60,
      left: 50,
      width: 200,
      height: 200,
      child: Container(
        width: 90,
        height: 90,
        color: Colors.red[400],
        child: Text(
          'Red',
          style: TextStyle(color: Colors.white, fontSize: 20),
        ),
      ),
    ),
    Positioned(
      top: 100,
      left: 75,
      width: 200,
      height: 200,
      child: Container(
        width: 80,
        height: 80,
        color: Colors.indigo[300],
        child: Text(
          'Blue',
          style: TextStyle(color: Colors.white, fontSize: 20),
        ),
      ),
    ),
  ],
),
...
```

<img src="{{ site.base_url }}/assets/images/positioned-widget-flutter/stack_positioned_app.png" class="img img-center img-50-imp" alt="stack-app-flutter">

As you can see in the example, we were able to place all the three containers using `Positioned` widget.


[flutter]: /assets/images/shared/flutter-sapidlabs.jpg
