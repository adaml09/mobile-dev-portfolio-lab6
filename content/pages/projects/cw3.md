---
type: ProjectLayout
title: Class Work 3
date: '2024-12-12'
client: Durham College
description: >-
  Class work 3, was similar to the first except this time we used Dart and
  flutter. It displays some basic information and was a way to get us started in
  this language. 
featuredImage:
  type: ImageBlock
  url: /images/CW3_1.png
  altText: CW3
  caption: ''
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
CW3

Adam LeBlanc

100818716

INFT-3101-01 Mobile Development

Mohammad Shamas

2024-11-15

# Flutter Code

import 'package:flutter/material.dart';\
import 'package:google\_fonts/google\_fonts.dart';\ <br/><br/>void main() {\
runApp(const MainApp());\
}\ <br/>class MainApp extends StatelessWidget {\
const MainApp({super.key});\ <br/>@override\
Widget build(BuildContext context) {\
return MaterialApp(\
home: Scaffold(\
body: Container(\
decoration: const BoxDecoration(\
image: DecorationImage(\
image: AssetImage('assets/background.png'),\
fit: BoxFit.cover,\
),\
),\
child: Center(\
child: Column(\
mainAxisAlignment: MainAxisAlignment.center,\
children: \[\
Text('Name: Adam LeBlanc', style: GoogleFonts.*pacifico*(fontSize: 35),),\
Text('ID: 100818716', style: GoogleFonts.*pacifico*(fontSize: 35), ),\
Text('INFT-3101-01 Mobile Development', style: GoogleFonts.*pacifico*(fontSize: 25),),\
Text('Favourite Quote:', style: GoogleFonts.*pacifico*(fontSize: 35),),\
Text('All hockey players are bilingual. They know English and profanity. - Grodie Howe', style: GoogleFonts.*pacifico*(fontSize: 20),)\
],\
),\
),\
),\
),\
);\
}\
}

# Screenshots

This is the app running in the android studio emulator:

![](/images/CW3_1.png)

This is the code running on my phone:

![](/images/CW3_2.png)

# Reflection

This assignment was a good way of introducing myself to the flutter coding environment. The download process seemed like it was going to be complicated at first but, thankfully it was relatively simple. Although it was a bit lengthy, I didn’t encounter any issues. Once it was downloaded making the actual app itself was a bit more difficult. The syntax of Dart was confusing at first, I also started with a template which was more complicated than this assignment required which made things that much more difficult. Once I opened one of the simpler project types I was able to figure out how to display what I wanted. The other issue that occurred was with the font, I used Google fonts for the font style. This worked fine when running in the android studio emulator, but when I tried to run it on my phone it showed up as regular text. Unfortunately, I couldn’t fix this issue for this assignment, but it shows that there is still more to learn when working with Flutter and Dart. That is something that I’m looking forward to doing later in the course as well as in my own time.
