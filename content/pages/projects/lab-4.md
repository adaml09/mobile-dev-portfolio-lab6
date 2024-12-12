---
type: ProjectLayout
title: Lab 4
date: '2024-12-12'
client: Durham College
description: >-
  Lab 4 was our first introduction to Dart. Each student was given a topic and
  the one that I got was objects.
featuredImage:
  type: ImageBlock
  url: /images/dart_logo_lab4.png
  altText: Project thumbnail image
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
media:
  type: ImageBlock
  url: /images/dart_logo_lab4.png
  altText: Dart_logo
  caption: Caption of the image
  elementId: ''
---
Mobile Development

Dart Programming report

Objects

Adam LeBlanc

100818716

Mohammad Shamas

Durham College

Contents

[Overview 2](#_Toc181345171)

[Why use Objects? 2](#_Toc181345172)

[Advantages / Limitations 2](#_Toc181345173)

[Advantages 2](#_Toc181345174)

[Disadvantages 3](#_Toc181345175)

[References 3](#_Toc181345176)

[Code Examples 4](#_Toc181345177)

[Example 1 4](#_Toc181345178)

[Example 2 5](#_Toc181345179)

[Real World Example 7](#_Toc181345180)

# Overview

In general objects are key parts of any programming language. They are sections of code that contain data and functions. Many programming languages have objects as the central part of their system, this is called object-oriented programming (OOP). Dart falls into this category, everything down to the variables is treated as an object in dart, even null is treated as such. Why are objects a key part of so many languages including dart, what advantages do they provide, are there any disadvantages?

# Why use Objects?

There are many reasons for why objects have become such an integral part of not just Dart but so many other programming languages. The main reason is that it allows code to be more organized and concise, this especially helps when attempting to manage large projects.

Creating objects means that your code can be broken down into similar smaller parts. By including functionality such as properties and behaviors into classes, you can call an object of this class anywhere in the code, rather than rewriting all the code again and again.

This compounds with the use of inheritance. If a new class is related to a previous class, you can use inheritance and all the functions that are shared between the two classes will automatically be implemented in the second class. This allows you to only add the new features to the new class, thus keeping code simpler and more organized.

# Advantages / Limitations

Just like anything else, the utilization of objects in Dart comes with its own set of advantages and disadvantages.

## Advantages

- Encapsulation – Dart allows for encapsulation by the creation of private data types. This is done by using underscore in the prefix of the declaration. This allows for the selected data to be protected, keeping internal states and information secure
- Reusability – just like any other OOP language, the use of objects in dart allows for great modularity within your code. As discussed earlier this means that your code can stay more organized and allows you to write less lines of code. This is great for large scale projects.
- Darts asynchronous design – The Dart language is designed with asynchronous functionality in mind, using keywords like await and async. The utilization of objects allows for event driven functionality which works well with this asynchronous architecture.

## Disadvantages

- Performance – The creation and use of objects is relatively taxing on memory due to their need to keep track of both the data and any methods. This can mean that overuse of objects in key performance areas of a program can cause a loss of performance
- Complexity – Although in many ways using objects can greatly simplify any project. The one scenario in which this may not be the case is in simple small projects. Using too many objects and classes when this is not necessary can make code more cumbersome than needed.
- Lack of Multiple inheritance – Dart does not support a class from inheriting from more than one super class. This can greatly decrease the potential functionality of some classes. Although mixins aid in this issue this still does not provide the full functionality of multiple inheritance.

### References

Dart. (n.d.). _Classes_. Dart.dev. <https://dart.dev/language/classes>

GeeksforGeeks. (2021, April 5). _Dart - Classes and Objects_. GeeksforGeeks. <https://www.geeksforgeeks.org/dart-classes-and-objects/>

Javatpoint. (n.d.). _Dart Classes and Object_. Javatpoint. <https://www.javatpoint.com/dart-classes-and-object>

Sarkar, R. (2021, August 17). _Inheritance in Dart_. Medium. <https://rushalisarkar.medium.com/inheritance-in-dart-6dde3cdaa6c4>

# Code Examples

## Example 1

In the following code I created a simple car class. This class has only three variables and a constructor, so it is very simple. Although creating any more complicated class would follow the same steps. After creating the class I made one object instance of that class. After creating the instance of the class I print out the data that is stored in the class.

void main() {

Car myCar = Car("Chevrolet", "Camaro", 2023);

print("Make: ${myCar.make}, Model: ${myCar.model}, Year: ${myCar.year}");

}

class Car{

String? make;

String? model;

int? year;

Car (String make, String model, int year){

this.make = make;

this.model = model;

this.year = year;

}

}

This code outputs: Make: Chevrolet, Model: Camaro, Year: 2023

Creating and instantiating classes in dart seems familiar to me as I’ve worked with other OOP languages before. So, for anyone with previous coding experience, you should be able to get up to speed relatively quickly.

## Example 2

In this example I used mxins to allow for shared functionality over multiple different classes and objects. I built this in addition to the car class example, this time I added a truck and van class, as well as the mixin driving. This mixin is incorporated into all the related classes allowing all the types of vehicles to display that they are driving. This shows how mxiins can aid in patching the hole that is Darts lack of multi-inheritance.

void main() {

Car myCar = Car("Chevrolet", "Camaro", 2023);

print("Make: ${myCar.make}, Model: ${myCar.model}, Year: ${myCar.year}");

Truck myTruck = new Truck();

Van myVan = new Van();

myCar.driveCar();

myTruck.driveTruck();

myVan.driveVan();

}

mixin IsDriving{

void drive() {

print("Driving zoom zoom");

}

}

class Car with IsDriving{

String? make;

String? model;

int? year;

Car (String make, String model, int year){

this.make = make;

this.model = model;

this.year = year;

}

void driveCar(){

print("Car");

drive();

}

}

class Truck with IsDriving{

void driveTruck(){

print("Truck");

drive();

}

}

class Van with IsDriving{

void driveVan(){

print("Van");

drive();

}

}

The output of this code is:

Make: Chevrolet, Model: Camaro, Year: 2023

Car

Driving zoom zoom

Truck

Driving zoom zoom

Van

Driving zoom zoom

This shows that mixins can be a solid replacement for multiple inheritance. Although coming from other languages where this was possible means that switching to mixins has been a bit of a learning curve.

# Real World Example

A real-world example where the use of objects would be useful in a Dart application would be an school management system. In this scenario, you could have classes to hold data and functions for students, teachers, classes, courses, grades or even more. This would allow you to simplify your code rather than having to repeat different lines each time a function related to one of these is needed. As in this kind of application things like accessing data and other information are required a lot. So having functionality in object instances of classes for this would make things much easier.