---
type: ProjectLayout
title: Lab 5
date: '2024-12-12'
client: Awesome client
description: >-
  Lab 5 was about getting us prepared for our first Flutter app. We once again
  were assigned a topic in flutter to research, the one I received was handling
  gestures in Flutter. 
featuredImage:
  type: ImageBlock
  url: /images/dart_logo_lab5.png
  altText: Dart_logo_lab5
  caption: >-
    source:
    https://www.google.com/url?sa=i&url=https%3A%2F%2Fwww.logo.wine%2Flogo%2FDart_%2528programming_language%2529&psig=AOvVaw20yInt6Gi79F9CcWCxgWn-&ust=1734070476861000&source=images&cd=vfe&opi=89978449&ved=0CBQQjRxqFwoTCPDdn4jKoYoDFQAAAAAdAAAAABAE
  elementId: ''
media:
  type: ImageBlock
  url: /images/dart_logo_lab5.png
  altText: dart_logo_lab5
  caption: >-
    Source:
    https://www.google.com/url?sa=i&url=https%3A%2F%2Fwww.logo.wine%2Flogo%2FDart_%2528programming_language%2529&psig=AOvVaw20yInt6Gi79F9CcWCxgWn-&ust=1734070476861000&source=images&cd=vfe&opi=89978449&ved=0CBQQjRxqFwoTCPDdn4jKoYoDFQAAAAAdAAAAABAE
  elementId: ''
addTitleSuffix: true
colors: colors-a
backgroundImage:
  type: BackgroundImage
  url: /images/bg2.jpg
  backgroundSize: cover
  backgroundPosition: center
  backgroundRepeat: no-repeat
  opacity: 100
---
Lab 5

Handling Gestures in Flutter

Adam LeBlanc

100818716

Mohammad Shamas

Durham College

# Overview

In mobile development there are different things that we need to lookout for. Normal programs only must worry about a mouse click or something that is typed on a keyboard, in mobile development due to the touch screens that these devices have there are other ways users interact with the program. These include swipes, taps, drags and other scaling motions. Since flutter is meant to be used for mobile development it has a designated way to deal with these types of interactions. This is with the use of pointers and gestures.

The method that Flutter uses to manage touch interactions with the program is divided into two sections. The first section or layer is raw pointer events which describe the location as well as the direction of pointers across the screen. The second section contains things know as gestures which describe the semantics of the interaction and are comprised of multiple different pointer movements.

This is extremely important to the mobile development process; all the modern smart devices utilize touch screens. So, all interaction with any app is done through them. Regular things like typing and taping are simple enough to navigate. More complicated gestures like swipe, drag pinches and more can be much more complicated to deal with. Flutter having a relatively simple way to deal with such interactions makes the mobile development process so much easier.

## Advantages and Disadvantages

### Advantages

- Unified gesture detection: Flutter provides a way to handle gesture interactions the same way across all platforms (IOS, Android and desktop). This means that you can keep your code more consistent and concise. As well as not having to worry about the program knowing what device it is on.
- Ease of use: Due to the functions such as GestureDetector, Draggable, and Dismissible, which are provided by flutter, gesture handling is made into a simple process. In addition to this you can also create custom gestures by combing the use of these premade functions.

### Disadvantages

- Overlapping gesture conflicts: Although customizability of the gestures can be a great aid, it can also be a source of issues. Since creating custom gestures is done by combining the already provided options, there is the possibility that certain conflicts can occur. This can make your app confusing and difficult to use.
- Performance impact: Along with the potential conflict issues, misuse and overuse of gesture detectors can create a harmful performance impact on your program. It is important to ensure that you are only detecting and handling the gestures that are necessary for your program to work.

# Coding Examples

In this example I used the online flutter code editor on dart.dev, I modified the base hello world code. Now the hello world text is wrapped in a GestureDector which detects any taps on it. When the hello world text is taped a string is printed in the console displaying “Text tapped!’. This is very basic, but it shows how in a simple form how a gesture detector widget in flutter works.

import 'package:flutter/material.dart';

void main() {

runApp(const MyApp());

}

class MyApp extends StatelessWidget {

const MyApp({super.key});

@override

Widget build(BuildContext context) {

return MaterialApp(

debugShowCheckedModeBanner: false,

home: Scaffold(

body: Center(

child: GestureDetector(

onTap: () {

print('Text tapped!');

},

child: const Text(

'Hello, World!',

style: TextStyle(

fontSize: 24,

color: Colors.blue,

decoration: TextDecoration.underline,

),

),

),

),

),

);

}

}

In the next example I further expanded on the last example, by adding multiple gesture widgets to the same text. Now the text can be tapped once, twice or held and get a different response.

import 'package:flutter/material.dart';

void main() {

runApp(const MyApp());

}

class MyApp extends StatelessWidget {

const MyApp({super.key});

@override

Widget build(BuildContext context) {

return MaterialApp(

debugShowCheckedModeBanner: false,

home: Scaffold(

body: Center(

child: GestureDetector(

onTap: () {

print('Text tapped!');

},

onLongPress: () {

print('Text tapped for a while!');

},

onDoubleTap: () {

print('Text tapped twice!');

},

child: const Text(

'Hello, World!',

style: TextStyle(

fontSize: 24,

color: Colors.blue,

decoration: TextDecoration.underline,

),

),

),

),

),

);

}

}

# Real World Example

A real-world example where the handling of gestures could be useful would be in an online sales app like Kijiji. An app like this would function a bit like a web page while incorporating multiple screens as well as ways you can interact with these screens. Without the way that flutter uses pointers to control this aspect of interacting with the screens this would be a very complicated application to create. With the pointer system that flutter implements, you would be able to make full use of this functionality in a concise and simple way. This would mean that you can get the most out of this and have the most fluid interactions possible with the app, while also using all of the phone’s touch features.

body: GestureDetector(

onHorizontalDragEnd: (DragEndDetails details) {

if (details.primaryVelocity! > 0) {

Navigator.pop(context);

}

This code snippet shows how the onHorizontalDragEnd gesture detector can be used to help add a swipe right to go back functionality. The if statement that checks for the primaryVelocity is used to check which way the swipe was directed. If it is a swipe to the right, it uses Navigator.pop which is a function that flutter uses to switch back to the previous screen.

# Sources

- <https://docs.flutter.dev/ui/interactivity/gestures>
- <https://www.geeksforgeeks.org/flutter-gesturedetector-widget/>
- <https://dart.dev/#try-dart>