---
type: ProjectLayout
title: Class Work 1
date: '2024-12-12'
client: Durham College
description: >-
  The class works were meant to be a short way to test the skills that we had
  been learning in the course. The first was to make a very simple app in
  android studio with XML and Java. 
featuredImage:
  type: ImageBlock
  url: /images/CW1_1.png
  altText: CW1_1
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
INFT-3101-01

Class Work 1 Report

Adam LeBlanc

100818716

Mohammad Shamas

2024-09-26

# Reflection

This class work was a great way to get started using android studio. As well as having the prior XML knowledge it made it a lot easier to get to grips with the basics of developing mobile apps. Overall, it was simple, the only requirements being that we display some basic data. Not having to have buttons made it much easier, although I’m sure we will do this in the future. This made me excited to take this farther and expand my knowledge on making apps using android studio. The only area that gave some difficulty was the external testing process. I originally was going to use Genymotion but, when I attempted to run the emulator, it kept failing. So, since I have an android phone myself, I uploaded to my phone and use that for the testing. Other than that small hiccup this was a simple and good way of introducing Android Studio and I look forward to learning more.

# Code

## XML

<?xml version="1.0" encoding="utf-8"?>\
<androidx.constraintlayout.widget.ConstraintLayout xmlns:android="<http://schemas.android.com/apk/res/android>"\
xmlns:app="<http://schemas.android.com/apk/res-auto>"\
xmlns:tools="<http://schemas.android.com/tools>"\
android:id="@+id/main"\
android:layout\_width="match\_parent"\
android:layout\_height="match\_parent"\
android:background="@drawable/background\_image"\
tools:context=".MainActivity">\ <br/><TextView  
android:id="@+id/information_textView"  
android:layout_width="196dp"  
android:layout_height="23dp"  
android:text="Name: Adam LeBlanc"  
android:textColor="#FF9800"  
android:textSize="20sp"  
app:layout_constraintBottom_toBottomOf="parent"  
app:layout_constraintEnd_toEndOf="parent"  
app:layout_constraintHorizontal_bias="0.423"  
app:layout_constraintStart_toStartOf="parent"  
app:layout_constraintTop_toTopOf="parent"  
app:layout_constraintVertical_bias="0.142" />\ <br/><TextView  
android:id="@+id/banner_textView"  
android:layout_width="229dp"  
android:layout_height="34dp"  
android:text="Banner ID: 100818716"  
android:textColor="#FFC107"  
android:textSize="20sp"  
app:layout_constraintBottom_toBottomOf="parent"  
app:layout_constraintEnd_toEndOf="parent"  
app:layout_constraintStart_toStartOf="parent"  
app:layout_constraintTop_toTopOf="parent"  
app:layout_constraintVertical_bias="0.2" />\ <br/><TextView  
android:id="@+id/class_textView"  
android:layout_width="259dp"  
android:layout_height="59dp"  
android:text="Class / Section: INFT-3101-01"  
android:textColor="#FF9800"  
android:textSize="20sp"  
app:layout_constraintBottom_toBottomOf="parent"  
app:layout_constraintEnd_toEndOf="parent"  
app:layout_constraintHorizontal_bias="0.598"  
app:layout_constraintStart_toStartOf="parent"  
app:layout_constraintTop_toTopOf="parent"  
app:layout_constraintVertical_bias="0.291" />\ <br/><TextView  
android:id="@+id/quote_textView"  
android:layout_width="259dp"  
android:layout_height="93dp"  
android:fontFamily="cursive"  
android:text="My Favourite Quote: What's behind you doesn't matter - Enzo Ferrari"  
android:textColor="#FFC107"  
android:textSize="20sp"  
app:layout_constraintBottom_toBottomOf="parent"  
app:layout_constraintEnd_toEndOf="parent"  
app:layout_constraintHorizontal_bias="0.598"  
app:layout_constraintStart_toStartOf="parent"  
app:layout_constraintTop_toTopOf="parent"  
app:layout_constraintVertical_bias="0.451" />\ <br/></androidx.constraintlayout.widget.ConstraintLayout>

## Java

package com.example.cw1\_adamleblanc;\ <br/>import android.os.Bundle;\ <br/>import androidx.activity.EdgeToEdge;\
import androidx.appcompat.app.AppCompatActivity;\
import androidx.core.graphics.Insets;\
import androidx.core.view\.ViewCompat;\
import androidx.core.view\.WindowInsetsCompat;\ <br/>public class MainActivity extends AppCompatActivity {\ <br/>@Override\
protected void onCreate(Bundle savedInstanceState) {\
super.onCreate(savedInstanceState);\
EdgeToEdge.*enable*(this);\
setContentView(R.layout.*activity\_main*);\
}\
}

# Testing Photos

Figure 1: Internal testing on Android Studio

![](/images/virtual_test_CW1.png)

Figure 2: External testing on my phone

![](/images/external_test_CW1.jpg)
